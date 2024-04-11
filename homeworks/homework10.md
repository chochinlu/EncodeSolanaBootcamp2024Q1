## Homework #10

#### Q 1:

Try a simple client transaction in Solana playground (https://beta.solpg.io/)
1. Make sure you are connected to the devnet and you have a wallet set up
2. Run the default client code, this will tell you your balance.
3. Create an airdrop signature and request the airdrop from the connection object `pg.connection.requestAirdrop`  you will need to add your public key and the number of lamports you want.
4. Use `await pg.connection.confirmTransaction;` to confirm the transaction.

#### A:

Add the following code to claim the air drop: 

``` typescript
console.log("Getting some airdrop....");
const signature = await pg.connection.requestAirdrop(
  pg.wallet.publicKey,
  LAMPORTS_PER_SOL
);

await pg.connection.confirmTransaction(signature);
console.log(`My balance: ${balance / web3.LAMPORTS_PER_SOL} SOL`);
```


#### Q 2:

1. Make sure your wallet is connected to the dev network
2. Try the airdrop to give yourself some SOL
3. Try to sign a message

Try altering the code to send a transaction to send to a hardcoded address
You can create a public key from a String, such as `5xot9PVkphiX2adznghwrAuxGs2zeWisNSxMW6hU6Hkj`


#### A:

Add the following code continuously:

``` typescript
let lamports = web3.LAMPORTS_PER_SOL / 100;

let toAccountPubkey = new web3.PublicKey(
  "GBwEBtgDn2rjweyfpkNGujU7prLiEXnAtdhoVgxq6Lie"
);
console.log(
  `Send ${lamports} lamports to account: ${toAccountPubkey.toString()}`
);

// Get latest blockhash info
const blockhashInfo = await pg.connection.getLatestBlockhash();

// Create transaction
const tx = new web3.Transaction({
  ...blockhashInfo,
});

// Add our hello world program instruction
tx.add(
  web3.SystemProgram.transfer({
    fromPubkey: pg.wallet.publicKey,
    toPubkey: toAccountPubkey,
    lamports,
  })
);

// Sign transaction
tx.sign(pg.wallet.keypair);

// Send the transaction to the Solana cluster
const txHash = await pg.connection.sendRawTransaction(tx.serialize());
console.log("Transaction hash: ", txHash);
```

Run and get the result: 

``` console
Running client...
  client.ts:
    My address: 6ijbDxeHVSUBDyNmrHLdXxYrrAdqKw7KpTNjQSHrw2wk
    My balance: 9.17836836 SOL
    Send 10000000 lamports to account: GBwEBtgDn2rjweyfpkNGujU7prLiEXnAtdhoVgxq6Lie
    Transaction hash:  enXJzn33Y5TMFstkc9JpzunW1htZDYkqPV2btAmdRQzZWfZWrV1s5QgAPLHMEaxXnBNBGQZrtUKDTYkFdURabHR
```