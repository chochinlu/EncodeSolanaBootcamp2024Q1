## Homework #8

### Solana Tokens
#### Q: 
1. Follow the instructions from the lesson and use the spl-token-cli to create
    -  A fungible token with a supply of 10,000
    -  An NFT
2. Try sending these tokens to others in your team , and use the command line to find details about the tokens.
3. Try sending using both the transfer and transfer --fund-recipient approach.

#### A:

Creating a fungible token:

``` console
~ spl-token create-token
Creating token CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX under program TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA

Address:  CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX
Decimals:  9

Signature: 4jiHPJ1dcjkmqzApGitvYPACwXv3astuJTFK7GFn1z5pcgJNEK6F3vd6piydniCVdsssVqL1JZLuxyT6u48aa8jv

~ spl-token supply CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX
0

~ spl-token create-account CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX
Creating account AQTM7NSB7dZuEDm2sJ6cdGYk5qn8Jxb972rfJiyPFmTB

Signature: 66LrhUSfwtkakoB6Sh1eRdg5mf9f1W6ywBJKD1wzq3Cjve9fdbuvsoUYEEkWni9qvMnokiV9P6ava5u3RZE14ZgT

~  spl-token mint CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX 10000
Minting 10000 tokens
  Token: CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX
  Recipient: AQTM7NSB7dZuEDm2sJ6cdGYk5qn8Jxb972rfJiyPFmTB

Signature: 5333kmZNuVwyVCr6SjimtFaKY6DXWgd2aJFBe9PfNU2pt5umK6iH2q9q715WXrDLaMRDvisUCctGHARagbPpvNK3

~ spl-token balance CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX
10000

~ spl-token accounts
Token                                         Balance
-----------------------------------------------------
CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX  10000
FpE2NeHa3y3suV8wRfN9zofFtdG8DWsQZhCJ6mk5eD3Y  20

~ spl-token transfer --fund-recipient CqhTU9FPHcetd9h35iwwDbXyiQFLL183mcRDpJLYiZXX 50 GBwEBtgDn2rjweyfpkNGujU7prLiEXnAtdhoVgxq6Lie
Transfer 50 tokens
  Sender: AQTM7NSB7dZuEDm2sJ6cdGYk5qn8Jxb972rfJiyPFmTB
  Recipient: GBwEBtgDn2rjweyfpkNGujU7prLiEXnAtdhoVgxq6Lie
  Recipient associated token account: 5sw75MP7XV5Vej5ax84AL7EcfotMWFcMgbQm1HdnqE75
  Funding recipient: 5sw75MP7XV5Vej5ax84AL7EcfotMWFcMgbQm1HdnqE75

Signature: 3BaowvcAQfXbM88nkaBZJDTdUhYPdxs6udcPpBFyvAZAkjvrFCBkGDyE4voPJaDS5bWrK5MX1crzQXZozMEQ9JBM

~ spl-token balance --address 5sw75MP7XV5Vej5ax84AL7EcfotMWFcMgbQm1HdnqE75
50
~ spl-token balance --address  AQTM7NSB7dZuEDm2sJ6cdGYk5qn8Jxb972rfJiyPFmTB
9950
```

Creating a non-fungible token: 

``` console
~ spl-token create-token --decimals 0
Creating token 6iZtv1pUUPAuBnTUZpD4PzMzkV1b5yBoVBCkHWa1k7xM under program TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA

Address:  6iZtv1pUUPAuBnTUZpD4PzMzkV1b5yBoVBCkHWa1k7xM
Decimals:  0

Signature: 3sKLPAbQsy3C7Yybc94VdsA84WL7SabYLBNKAGH2zGf5kqoby3hrKYSkcT8ZexHozXkz2xgeLPAAsT7ZuUQacdKx

~ spl-token create-account 6iZtv1pUUPAuBnTUZpD4PzMzkV1b5yBoVBCkHWa1k7xM
Creating account 2imdUQgMvLPfQBg7YMR8WcuiQe7pou5u3rQciTiz1gTw

Signature: 42m3SuBAN3m3Qv3Luxq4ASQBxB4GVmfkxNfN8WzYwAydE6WqrckHgYQC2pxKyEwsQS6fx5Y55FNRx6zbwWMKqJw2

~  spl-token mint 6iZtv1pUUPAuBnTUZpD4PzMzkV1b5yBoVBCkHWa1k7xM 1 2imdUQgMvLPfQBg7YMR8WcuiQe7pou5u3rQciTiz1gTw
Minting 1 tokens
  Token: 6iZtv1pUUPAuBnTUZpD4PzMzkV1b5yBoVBCkHWa1k7xM
  Recipient: 2imdUQgMvLPfQBg7YMR8WcuiQe7pou5u3rQciTiz1gTw

Signature: FNkxRCxQvFaa765A3pqiJ47YoqQVbAvRf8r6WGbgzNtzj5h6B6eNexABehbsQServanSHAzbqKybAtnd9vwoMM5

~ spl-token balance --address 2imdUQgMvLPfQBg7YMR8WcuiQe7pou5u3rQciTiz1gTw
1

~ spl-token account-info --address 2imdUQgMvLPfQBg7YMR8WcuiQe7pou5u3rQciTiz1gTw

SPL Token Account
  Address: 2imdUQgMvLPfQBg7YMR8WcuiQe7pou5u3rQciTiz1gTw
  Program: TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA
  Balance: 1
  Decimals: 0
  Mint: 6iZtv1pUUPAuBnTUZpD4PzMzkV1b5yBoVBCkHWa1k7xM
  Owner: 6ijbDxeHVSUBDyNmrHLdXxYrrAdqKw7KpTNjQSHrw2wk
  State: Initialized
  Delegation: (not set)
  Close authority: (not set)
```

Transfer the NFT to the anther account: 

``` console
~ spl-token transfer --fund-recipient 6iZtv1pUUPAuBnTUZpD4PzMzkV1b5yBoVBCkHWa1k7xM 1 GBwEBtgDn2rjweyfpkNGujU7prLiEXnAtdhoVgxq6Lie
Transfer 1 tokens
  Sender: 2imdUQgMvLPfQBg7YMR8WcuiQe7pou5u3rQciTiz1gTw
  Recipient: GBwEBtgDn2rjweyfpkNGujU7prLiEXnAtdhoVgxq6Lie
  Recipient associated token account: 8kV2GKk2i2SXVZPsg4y9oujaV7pN1XXQ6zwNWfgri1sD
  Funding recipient: 8kV2GKk2i2SXVZPsg4y9oujaV7pN1XXQ6zwNWfgri1sD

Signature: 28hhEMcQB6XSN6w3xdU3dxLYE8TJnVoYpU5D3ohunMM6NfiwViZAymsRNLzX6m5CBukzXz72DzgLvWLMMRu9WUfW

~ spl-token account-info --address 8kV2GKk2i2SXVZPsg4y9oujaV7pN1XXQ6zwNWfgri1sD

SPL Token Account
  Address: 8kV2GKk2i2SXVZPsg4y9oujaV7pN1XXQ6zwNWfgri1sD
  Program: TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA
  Balance: 1
  Decimals: 0
  Mint: 6iZtv1pUUPAuBnTUZpD4PzMzkV1b5yBoVBCkHWa1k7xM
  Owner: GBwEBtgDn2rjweyfpkNGujU7prLiEXnAtdhoVgxq6Lie
  State: Initialized
  Delegation: (not set)
  Close authority: (not set)

~ spl-token balance --address 2imdUQgMvLPfQBg7YMR8WcuiQe7pou5u3rQciTiz1gTw
0
```

### Solana Programs

#### Q:
Using the examples in the repo
1. Modify the existing msg! in example1- helloworld to log the program ID.
2. Retrieve the total program size of example1-helloworld.
3. Retrieve the lamport balance of example2- counter.
4. Modify the client for example2-counter to feed an incorrect address for the greeting

#### A(1): 

Update the content of `msg!` :

``` rust
    msg!(
        "[lib] Hello World Rust program entrypoint. ==> Program ID: {}",
        _program_id
    );
```

Build and deploy the code:

``` console
~ cargo build-bpf --workspace --manifest-path=/home/park/wsl_codes/solana_test/SolanaBootcamp/examples_baremetal/Cargo.toml
~ solana program deploy /home/park/wsl_codes/solana_test/SolanaBootcamp/examples_baremetal/target/deploy/helloworld.so
```



Run the client: 

``` console
~ ts-node ./examples_baremetal/example1-helloworld/client/main.ts

local system client config location:  /home/park/.config/solana/cli/config.yml  

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 4033350765, 'solana-core': '1.16.21' }

It cost:
        0.000004947185516357422 SOL
        4992 Lamports
to perform the call
```


`solana logs`: 

``` console
Transaction executed in slot 3341:
  Signature: 57aPGfJMiw4GCYeeBVeKhsWsJPiRgo93mMuYyx2PkLJXxkiW8M5hEBoX5JRg9ybMJBmT2GvUJE8HbCeJrbW93ydN
  Status: Ok
  Log Messages:
    Program CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4 invoke [1]
    Program log: [lib] Hello World Rust program entrypoint. Program ID: CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4
    Program CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4 consumed 11930 of 200000 compute units
    Program CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4 success
```

#### A(2): 

Check the length of the program account: 

``` console
~/wsl_codes/solana_test/SolanaBootcamp(main U:1 ✗) solana account CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4

Public Key: CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4
Balance: 0.00114144 SOL
Owner: BPFLoaderUpgradeab1e11111111111111111111111
Executable: true
Rent Epoch: 18446744073709551615
Length: 36 (0x24) bytes
0000:   02 00 00 00  d0 53 ff 14  ce 11 23 91  50 d2 03 ac   .....S....#.P...
0010:   49 de 02 8c  eb 91 7f bc  d7 3c c9 a4  dd 0b 49 08   I........<....I.
0020:   19 8a 65 39
```

The lenth of the program is 36 bytes. 


#### A(3): 

Deploy the program:

``` console
 ~/wsl_codes/solana_test/SolanaBootcamp(main U:2 ✗) npm run deploy:2

> solana-course@0.0.1 deploy:2
> solana program deploy ./examples_baremetal/target/deploy/counter.so

Program Id: CGJZSQqBe96BTUM6kJcwLuUA4XtwLgEoGLFAkNC289zr                                                                    
~/wsl_codes/solana_test/SolanaBootcamp(main U:2 ?:1 ✗) npm run call:2

> solana-course@0.0.1 call:2
> ts-node examples_baremetal/example2-counter/client/main.ts

Let's increment counter for an account!

local system client config location:  /home/park/.config/solana/cli/config.yml

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 4033350765, 'solana-core': '1.16.21' }
Program ID account:  CGJZSQqBe96BTUM6kJcwLuUA4XtwLgEoGLFAkNC289zr
Account 5dnWXpErTK1cyEnM1YRTFkjhYzmsv19Toqt24hrqz359 not deployed, deploying now
Creating account 5dnWXpErTK1cyEnM1YRTFkjhYzmsv19Toqt24hrqz359 to say hello to
5dnWXpErTK1cyEnM1YRTFkjhYzmsv19Toqt24hrqz359 has been greeted 0 time(s)

It cost:
        0.0009236931800842285 SOL
        923712 Lamports
to perform the call
```

Get the balace of this program account : 

``` console
~/wsl_codes/solana_test/SolanaBootcamp(main U:2 ?:1 ✗)  solana balance --lamports CGJZSQqBe96BTUM6kJcwLuUA4XtwLgEoGLFAkNC289CGJZSQqBe96BTUM6kJcwLuUA4XtwLgEoGLFAkNC289zr
1141440 lamports
```

#### A(4):

Just add the incorrect key as the pubkey:

``` rust
    const INCORRECT_KEY = PublicKey.default;

    const instruction = new TransactionInstruction({
      keys: [{ pubkey: INCORRECT_KEY, isSigner: false, isWritable: true }],
      programId,
      data: Buffer.alloc(0), // All instructions are hellos
    });
```


Call the program: 

```
~/wsl_codes/solana_test/SolanaBootcamp(main U:2 ?:1 ✗) npm run call:2

> solana-course@0.0.1 call:2
> ts-node examples_baremetal/example2-counter/client/main.ts

Let's increment counter for an account!

local system client config location:  /home/park/.config/solana/cli/config.yml

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 4033350765, 'solana-core': '1.16.21' }
Program ID account:  CGJZSQqBe96BTUM6kJcwLuUA4XtwLgEoGLFAkNC289zr
Writing to the greeting counter 5dnWXpErTK1cyEnM1YRTFkjhYzmsv19Toqt24hrqz359
INCORRECT_KEY:  PublicKey { _bn: <BN: 0> }
Transaction simulation failed: Error processing Instruction 0: incorrect program id for instruction
    Program CGJZSQqBe96BTUM6kJcwLuUA4XtwLgEoGLFAkNC289zr invoke [1]
    Program log: [lib] Solana Example2 counter program entrypoint
    Program log: [lib] hello account: 11111111111111111111111111111111
    Program log:  Greeted account does not have the correct program id
```