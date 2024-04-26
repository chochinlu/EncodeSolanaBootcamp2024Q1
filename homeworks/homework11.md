## Homework #11

#### Q 1: 

1. Use the Anchor command line tools to create a new project.
2. Adapt the default program as follows 1. In an account we want to store a balance of type u64
2. On initialisation, this balance should be set to 100
3. Write a test to check that the balance was initialised correctly.


#### A:

[Reference answer](https://github.com/mmsaki/solana-storage/blob/master/tests/storage.ts)

[My Repo](https://github.com/chochinlu/hw_11)


##### Q 2: 

From the Bootcamp repo, [anchor examples](https://github.com/ExtropyIO/SolanaBootcamp/tree/main/examples_anchor)

1. Modify the lottery program so that the payout is only 90% of the total deposits.
2. Add a function that allows lottery admin to withdraw funds after the winner is picked.


## Homework #12

Further develop the anchor program you started
in the last homework
1. Add a function to allow the balance to be updated in steps of 100 up to a maximum of 1000.
2. If you try to update the balance when it is at its maximum value, throw a custom error with an appropriate error message.
3. What constraints should your program have ?

### A: 

[My Repo](https://github.com/chochinlu/hw_11)