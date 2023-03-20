# Fees

A $0.10 stable fee is added to each transaction\* and deducted from asset. You DO NOT need any native (MATIC) tokens to deposit, transfer, or withdraw from ZKPay. All tx fees are $0.10 and paid using selected token.

Fees cover the cost of transactions in most situations (_see below_) and can result in a surplus depending on gas and token prices. Fees accumulates with the fee receiver and is periodically withdrawn, and sent to the sequencer operator to subsidize future transaction costs. Sequencer operators do not keep any profits from extra fees - all excess fees are sent to the ZKPay DAO.&#x20;

\*_In special cases, transactions may incur additional fees when many notes need to be processed at the same time. Learn more._

### Transaction costs

Exact tx fees are calculated as the cost of the calldata for an operation (deposit, transfer, withdrawal) multiplied by the gas price and the token price. Tx gas examples:

* ZKPay deposit 783,638 gas
* ZKPay transfer 601,357 gas
* ZKPay withdrawal 620,679 gas

To calculate a baseline for any operation, we take the highest gas cost (deposit) + 15% buffer = 902,000 gas.

Max Fee baseline = `902,000 * gas price * token price`

Fees can vary significantly based on the gas price and token price at the time of a transaction. In this table, the top row shows example USD equivalent token prices ($0.35 to $1.05) and the left column shows varying gas costs ranging from 30 to 100 gwei. These are multiplied with 902,000 to calculate the cost for a max transaction.

|          | $0.35  | $0.80 | $1.05 |
| -------- | ------ | ----- | ----- |
| 30 gwei  | $0.009 | $0.02 | $0.03 |
| 75 gwei  | $0.02  | $0.05 | $0.07 |
| 100 gwei | $0.03  | $0.07 | $0.1  |

### Fee Collection

Fees are currently collected in the ZKPay Governance SAFE. Fees are withdrawn to cover sequencer operation expenses. Excess fees are left to the DAO to manage.

Additionally, interest earned from deposits supplied to Aave are stored in the ZKPay Governance SAFE. As the network continues to grow, this revenue stream will be managed by the DAO.

### View Accumulated Fees

Anyone can view current fees accumulated by the protocol.

Go to the Dune Dashboard
