
## Homework #1

#### Q: 1. Tell about your goals for this course

A: Familiar with the priciples of blockchain, especially Solana, and proficient in Rust programming. Utilizing these two skills to create original projects, finding joy in the process, and earning reasonable rewards.

#### Q: 2. Discuss in your teams what a decentralised version of a game like monopoly would be like, if there was no software on a central server. Consider What are the essential pieces of functionality ? How could people cheat ? How could you prevent them from cheating ? This is just a general discussion, there is no need to write any code or do any design.

A:

If it's a decentralized game like Monopoly:

- Players can participate from anywhere in the world.
- Transactions are secured using blockchain technology, ensuring immutability and transparency.
- Every transaction and game action is recorded on the blockchain, allowing anyone to verify the game's integrity.
- Smart contracts handle game logic and enforce rules, ensuring fairness and preventing cheating.
- The development company doesn't require ongoing maintenance, significantly reducing maintenance costs.(maybe)

I believe key mechanisms include:

- Players' contributions needing a third-party to store and execute transactions.
- Random mechanisms, including dice rolling and card drawing.
- Data records, including user porfiles, transaction logs, game progress, and past game results.

Areas where players might cheat include:

- Modifying amounts.

- Showing expenditure but not actually spending any funds.
- Tampering with probabilities.
- Fabricating historical records, awards, etc.

How to prevent cheating:

- An escrow account where funds are held in trust while two or more parties complete a transaction.
  All logic execution, including dice rolling and data recording, is handled by smart contracts, ensuring that no one can tamper with them arbitrarily.

#### Q: 3. Do you feel that Central Bank Digital Currencies (CBDCs) are a move towards decentralisation? Will they help or hinder adoption of other cryptocurrencies?

A:

Perhaps CBDCs can indeed be seen as a step towards decentralization. While CBDCs still belong to the category of centralized controlled currencies, it's also possible for them to adopt blockchain technology for issuance.

This allows more people to understand the concept of blockchain and accelerates the development of blockchain and related cryptocurrency technologies, such as security, privacy protection, and scalability. Whether CBDCs will hinder or help the adoption of cryptocurrencies primarily depends on the policies and implementations of central banks.

## Homework #2 Solana Ecosystem

#### Q: 1. How many validators are there currently ?

A: Based on the network activity in the past 24 hours, there are 1724 validators as of 2024/3/27. ( https://solanabeach.io/validators )

#### Q: 2. What is special about this block https://explorer.solana.com/block/0 ?

A: the genesis block

#### Q: 3. What is special about this address https://explorer.solana.com/address/1nc1nerator11111111111111111111111111111111

A:

This address is indeed a specific address known as the "incinerator" in the Solana ecosystem. Its purpose is to permanently remove SOL tokens from circulation by "burning" them, making them unrecoverable. This process helps reduce the overall token supply and can have implications for factors like token scarcity and value.

While you can technically interact with this address, its primary function is to remove SOL tokens, so any transfers to it will effectively result in those tokens being permanently removed from circulation.

#### Q: 4. What is this transaction doing https://explorer.solana.com/tx/45pGoC4Rr3fJ1TKrsiRkhHRbdUeX7633XAGVec6XzVdpRbzQgHhe6ZC6Uq164MPWtiqMg7wCkC6Wy3jy2BqsDEKf ?

A: 11,365,066.99 SOL were burned.

#### Q: 5. What is the largest balance you can find in an account ?

A: ~~18446744073709551615 lamports. Solana uses the Rust u64 type.~~

#### Q: 6. What advantages will the end user see when using Solana compared to other blockchains ?

A: Transaction speed and low transaction fees.

## Homework #4 

[Fizz buzz program](https://github.com/chochinlu/hw4)

Result: 

```
Welcome!! It's a bootcamp homework #4
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
fizz
buzz
fizz
fizz
buzz
fizz
fizz buzz
Number of 'fizz buzz' occurred: 20
```

## Homework #5

[source](https://github.com/chochinlu/SolanaBootcamp/tree/main/homeworks_rust/homeworks/homework5)

``` console
⠉ Compiling homeworks/homework5/standard_library_types/iterators1.rs...
✓ Successfully ran homeworks/homework5/standard_library_types/iterators1.rs!
★ All exercises completed! ★

+----------------------------------------------------+
|          You made it to the End of this Homework!          |
+--------------------------  ------------------------+
                          \\/
     ▒▒          ▒▒▒▒▒▒▒▒      ▒▒▒▒▒▒▒▒          ▒▒
   ▒▒▒▒  ▒▒    ▒▒        ▒▒  ▒▒        ▒▒    ▒▒  ▒▒▒▒
   ▒▒▒▒  ▒▒  ▒▒            ▒▒            ▒▒  ▒▒  ▒▒▒▒
 ░░▒▒▒▒░░▒▒  ▒▒            ▒▒            ▒▒  ▒▒░░▒▒▒▒
   ▓▓▓▓▓▓▓▓  ▓▓      ▓▓██  ▓▓  ▓▓██      ▓▓  ▓▓▓▓▓▓▓▓
     ▒▒▒▒    ▒▒      ████  ▒▒  ████      ▒▒░░  ▒▒▒▒
       ▒▒  ▒▒▒▒▒▒        ▒▒▒▒▒▒        ▒▒▒▒▒▒  ▒▒
         ▒▒▒▒▒▒▒▒▒▒▓▓▓▓▓▓▒▒▒▒▒▒▒▒▓▓▒▒▓▓▒▒▒▒▒▒▒▒
           ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
             ▒▒▒▒▒▒▒▒▒▒██▒▒▒▒▒▒██▒▒▒▒▒▒▒▒▒▒
           ▒▒  ▒▒▒▒▒▒▒▒▒▒██████▒▒▒▒▒▒▒▒▒▒  ▒▒
         ▒▒    ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒    ▒▒
       ▒▒    ▒▒    ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒    ▒▒    ▒▒
       ▒▒  ▒▒    ▒▒                  ▒▒    ▒▒  ▒▒
           ▒▒  ▒▒                      ▒▒  ▒▒

We hope you enjoyed learning about the various aspects of Rust!
If you noticed any issues, please don't hesitate to report them to our repo.
You can also contribute your own exercises to help the greater community!

Before reporting an issue or contributing, please read our guidelines:
https://github.com/rust-lang/rustlings/blob/main/CONTRIBUTING.md
```

## Homework #6

[source](https://github.com/chochinlu/SolanaBootcamp/tree/main/homeworks_rust/homeworks/homework6)

```
✓ Successfully ran homeworks/homework6/option/option3.rs!
★ All exercises completed! ★
```

## Homework #7

[source](https://github.com/chochinlu/SolanaBootcamp/tree/main/homeworks_rust/homeworks/homework7)

```
✓ Successfully tested homeworks/homework7/tests/tests3.rs
★ All exercises completed! ★
```

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