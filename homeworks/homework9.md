## Homework #9

#### Q 1:
Work through the CPI example : example4-cpi. This program receives no instruction data, no accounts and it only logs a message using the msg! macro that can be viewed in the window running `solana logs


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

Only `Read program accounts` is workable:

``` console
~/wsl_codes/solana_test/SolanaBootcamp(main ✓) npm run call:6

> solana-course@0.0.1 call:6
> ts-node examples_baremetal/example6-pda/client/main.ts

Let's derive some accounts!

local system client config location:  /home/park/.config/solana/cli/config.yml

local system client config location:  /home/park/.config/solana/cli/config.yml
Connection to cluster established: http://localhost:8899 { 'feature-set': 4033350765, 'solana-core': '1.16.21' }
Pick option:
        Create PDA:     (1)
        Write PDA:      (2)
        Read PDA:       (3)
        Read program accounts:  (4)
4

5kcffa4SRMfzw74ah7vD3tWswaKQqfrJ38fhWwYvxTXP owns:


It cost:
        0 SOL
        0 Lamports
to perform the call
```

#### Q 4:

Anchor : Create a hello world project, follow [the instructions](https://book.anchor-lang.com/getting_started/hello_anchor.html)