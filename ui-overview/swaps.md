# Swaps

Users can swap assets deposited into the PolyAztec network using ZKPay's LP pools. The network does not support internal smart contracts and requires using liquidity on Polygon to help facilitate token swaps.

1inch is used to provide the user with the best market rate. The user must initiate a reservation with ZKPay's LP pool. A reservation locks in the exchange rate and ensures the token swap will complete successfully. \
\
The user must wait for the PolyAztec block to settle for the newly swapped tokens to appear in their zkAccount and become spendable. \
\
Supported private token swaps:

* zkDAI&#x20;
* zkETH
* zkMATIC
