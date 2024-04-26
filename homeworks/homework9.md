## Homework #9

#### Q 1:
Work through the CPI example : example4-cpi. This program receives no instruction data, no accounts and it only logs a message using the msg! macro that can be viewed in the window running `solana logs

### A: 

It's a CPI call, **we need to first confirm the hello-world program has been deployed**:

``` console
~/wsl_codes/solana_test/SolanaBootcamp(main → origin ↑6 S:1 ✗) npm run deploy:1

> solana-course@0.0.1 deploy:1
> solana program deploy ./examples_baremetal/target/deploy/helloworld.so

Program Id: CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4                                                                                                               
~/wsl_codes/solana_test/SolanaBootcamp(main → origin ↑6 S:1 ✗) npm run deploy:4

> solana-course@0.0.1 deploy:4
> solana program deploy ./examples_baremetal/target/deploy/cpi.so

Program Id: EEize3oTsV9x3j6fd9Z6Pxd1nrHjVYDrLNuurXUSFJGn                                                                                                               
~/wsl_codes/solana_test/SolanaBootcamp(main → origin ↑6 S:1 ✗) npm run call:4

> solana-course@0.0.1 call:4
> ts-node examples_baremetal/example4-cpi/client/main.ts

Let's invoke other program!

local system client config location:  /home/park/.config/solana/cli/config.yml

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 3469865029, 'solana-core': '1.18.9' }
programIDHelloWorld:  CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4

It cost:
        0.0000050067901611328125 SOL
        4992 Lamports
to perform the call
```

Solana logs: 

``` console
Transaction executed in slot 157:
  Signature: 3MZn9BVDf8M7pxT7aP2DG4MjRiQsvfCzZgvJw4M3vH53bZwtzCYpgqdGktg8wndN4qxKgeZcKB6MA2hDjkXynLi4
  Status: Ok
  Log Messages:
    Program EEize3oTsV9x3j6fd9Z6Pxd1nrHjVYDrLNuurXUSFJGn invoke [1]
    Program log: [entrypoint] CPI
    Program log: [entrypoint] Calling helloworld
    Program CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4 invoke [2]
    Program log: [lib] Hello World Rust program entrypoint. ==> Program ID: CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4
    Program CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4 consumed 11629 of 198433 compute units
    Program CfGc5msBQbGUZpCjuBf2oU86xNoFaWq4NASUpjZRAAu4 success
    Program EEize3oTsV9x3j6fd9Z6Pxd1nrHjVYDrLNuurXUSFJGn consumed 13252 of 200000 compute units
    Program EEize3oTsV9x3j6fd9Z6Pxd1nrHjVYDrLNuurXUSFJGn success
```



#### Q 2:
Work through the compute budget example

#### A:

``` console
Transaction executed in slot 772:
  Signature: 2gXU19CicgpLuq46z5pxSVSuBXVPPi7hdCzQwdqLnpuUZ76KviMFNoZWQhf8Ti6bVCQeEvGSWUDk41ZqM4kC7PRz
  Status: Ok
  Log Messages:
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV invoke [1]
    Program log: [entrypoint] compute example entrypoint
    Program log: [entrypoint] will find 1-prime
    Program log: 1 th prime number is 2
    Program log: 1 th prime number is 2
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV consumed 2490 of 200000 compute units
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV success
Transaction executed in slot 804:
  Signature: hskA5CgCKV1U6FriHCnw1e2ozPXpT6xkxtGhYGmCtPm86DT4ZoqGwQV1kLzWaN7k5FofVQjtrxtRza1B8Vv2nuv
  Status: Ok
  Log Messages:
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV invoke [1]
    Program log: [entrypoint] compute example entrypoint
    Program log: [entrypoint] will find 2-prime
    Program log: 1 th prime number is 2
    Program log: 2 th prime number is 3
    Program log: 2 th prime number is 3
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV consumed 3474 of 200000 compute units
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV success
Transaction executed in slot 887:
  Signature: 3YXMFHoiRoH5zbFnAy4DgKwRWLXTqwGUehXboAxtAU1hn3pGRvHLAg6qNeozXtinwdA1RtYiBRreKKj3FXUUbjpN
  Status: Ok
  Log Messages:
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV invoke [1]
    Program log: [entrypoint] compute example entrypoint
    Program log: [entrypoint] will find 3-prime
    Program log: 1 th prime number is 2
    Program log: 2 th prime number is 3
    Program log: 3 th prime number is 5
    Program log: 3 th prime number is 5
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV consumed 4811 of 200000 compute units
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV success
Transaction executed in slot 904:
  Signature: 4F8yXWvt3jXgBpsA67cySbYxT3KDSfqt19xM6mfyUiWjFgXRiU6CV4e5JFDDUekF3gXps8E4a1CytwZFfGgc5cvj
  Status: Ok
  Log Messages:
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV invoke [1]
    Program log: [entrypoint] compute example entrypoint
    Program log: [entrypoint] will find 8-prime
    Program log: 1 th prime number is 2
    Program log: 2 th prime number is 3
    Program log: 3 th prime number is 5
    Program log: 4 th prime number is 7
    Program log: 5 th prime number is 11
    Program log: 6 th prime number is 13
    Program log: 7 th prime number is 17
    Program log: 8 th prime number is 19
    Program log: 8 th prime number is 19
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV consumed 13186 of 200000 compute units
    Program BU3duCYeWXj9Pw1TM6Pk5ciQ799QUm1G1Tny8WFCDpzV success
```


#### Q 3:

Work through the PDA example : example6-pda


#### A:

Be careful the size of PDA we want to create: 

``` console
~/wsl_codes/solana_test/SolanaBootcamp(main → origin ↑6 S:1 U:2 ✗) npm run deploy:6

> solana-course@0.0.1 deploy:6
> solana program deploy ./examples_baremetal/target/deploy/pda.so

Program Id: 5kcffa4SRMfzw74ah7vD3tWswaKQqfrJ38fhWwYvxTXP

~/wsl_codes/solana_test/SolanaBootcamp(main → origin ↑6 S:1 U:2 ✗) npm run call:6

> solana-course@0.0.1 call:6
> ts-node examples_baremetal/example6-pda/client/main.ts

Let's derive some accounts!

local system client config location:  /home/park/.config/solana/cli/config.yml

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 3469865029, 'solana-core': '1.18.9' }
Pick option:
        Create PDA:     (1)
        Write PDA:      (2)
        Read PDA:       (3)
        Read program accounts:  (4)
1

Pick seed for account generation.
park

Pick account size in bytes.
100

Derived FffkWWHviwpfaWcMyA5rNB2LsVzLte4kvXnq2DYwS2Jj from park at 255 bump
Instruction byte train to send: park�d

It cost:
        0.0015919208526611328 SOL
        1591936 Lamports
to perform the call


~/wsl_codes/solana_test/SolanaBootcamp(main → origin ↑6 S:1 U:2 ✗) npm run call:6

> solana-course@0.0.1 call:6
> ts-node examples_baremetal/example6-pda/client/main.ts

Let's derive some accounts!

local system client config location:  /home/park/.config/solana/cli/config.yml

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 3469865029, 'solana-core': '1.18.9' }
Pick option:
        Create PDA:     (1)
        Write PDA:      (2)
        Read PDA:       (3)
        Read program accounts:  (4)
3
Provide seed for the account to read.
park

 FffkWWHviwpfaWcMyA5rNB2LsVzLte4kvXnq2DYwS2Jj contains:

It cost:
        0 SOL
        0 Lamports
to perform the call
~/wsl_codes/solana_test/SolanaBootcamp(main → origin ↑6 S:1 U:2 ✗) npm run call:6

> solana-course@0.0.1 call:6
> ts-node examples_baremetal/example6-pda/client/main.ts

Let's derive some accounts!

local system client config location:  /home/park/.config/solana/cli/config.yml

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 3469865029, 'solana-core': '1.18.9' }
Pick option:
        Create PDA:     (1)
        Write PDA:      (2)
        Read PDA:       (3)
        Read program accounts:  (4)
4

5kcffa4SRMfzw74ah7vD3tWswaKQqfrJ38fhWwYvxTXP owns:

FffkWWHviwpfaWcMyA5rNB2LsVzLte4kvXnq2DYwS2Jj

It cost:
        0 SOL
        0 Lamports
to perform the call
~/wsl_codes/solana_test/SolanaBootcamp(main → origin ↑6 S:1 U:2 ✗) npm run call:6

> solana-course@0.0.1 call:6
> ts-node examples_baremetal/example6-pda/client/main.ts

Let's derive some accounts!

local system client config location:  /home/park/.config/solana/cli/config.yml

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 3469865029, 'solana-core': '1.18.9' }
Pick option:
        Create PDA:     (1)
        Write PDA:      (2)
        Read PDA:       (3)
        Read program accounts:  (4)
2

Provide seed for the account to write to.
park
theAccountToWrite:  FffkWWHviwpfaWcMyA5rNB2LsVzLte4kvXnq2DYwS2Jj
Type string to write to the account.
> pppp

It cost:
        0.0000050067901611328125 SOL
        4992 Lamports
to perform the call
```




#### Q 4:

Anchor : Create a hello world project, follow [the instructions](https://book.anchor-lang.com/getting_started/hello_anchor.html)