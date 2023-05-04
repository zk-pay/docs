# Basic Concepts

### ZKPay Web App

ZKPay is a zk-based privacy application built for private transfers. It accepts DAI, ETH, and MATIC for deposit, and once deposited in the ZKPay app, zkAssets can be transferred anonymously between participants. zkAssets can then be withdrawn from the application to an EOA (externally owned address) preserving anonymity of the transfer amounts and participants.

### Zero-Knowledge Proofs (zkSNARKs)

PolyAztec uses zkSNARKS zero-knowledge proofs to verify an action has been completed (deposit, transfer, withdrawal) without providing any other identifying details about that action. zkSNARKs confirm that the chain state has changed without divulging information about amounts, initiators, or receivers of transactions. [Learn more about zero-knowledge proofs.](https://vitalik.ca/general/2021/01/26/snarks.html)

### ZKPay Account

A ZKPay account is linked to a user via a private key. The private key is used to identify the account balance, generate proofs to transfer tokens, and withdraw tokens from the network.&#x20;

ZKPay accounts are created from the private key of an existing MetaMask/WalletConnect/Web3 wallet. Users can decide how they would like to create an account following a step-by-step process.

Accounts never appear unencrypted in a public field and can only be decrypted by the account owner.

### ZKPay Address

A PolyAztec address contains a fixed shield address for receiving funds. The user generates a private shield address using the application and connects the address to an alias/username of their choosing.&#x20;

Only the account owner can confirm ownership of a private shield address.



### **Deposits**

Deposits can be made by sending tokens (from a regular 0x-based account) to the PolyAztec contract. Depositors complete 2 steps to get started.&#x20;

1. Approve the contract to move funds.
2. Create and send the deposit.&#x20;

Deposits are reflected in the users balance after the PolyAztec block settles.

### Sends

A user can send funds to another PolyAztec address by generating a zk-proof anonymously to the network. This consumes a note or multiple notes and the available spendable balance might show zero. The user must wait for the PolyAztec block to settle before sending again.

### Withdrawals

Similar to deposits, a user can create a zero-knowledge proof and provides it to the PolyAztec network to withdraw tokens from the PolyAztec network. The transaction contains a zero-knowledge proof of token ownership generated using the private key associated with the corresponding PolyAztec account.

### Liquidity Pool

The liquidity pool (LP pool) acts as an intermediary between the PolyAztec network and smart contracts on Polygon. Transactions are sent to the LP which collects transactions, orders them in a queue, then performs the action requested by the user. The LP cannot see which user has initiated the requested action.&#x20;

Currently, the LP is required for [swapping](../ui-overview/swaps.md) zkAssets stored inside the PolyAztec network.
