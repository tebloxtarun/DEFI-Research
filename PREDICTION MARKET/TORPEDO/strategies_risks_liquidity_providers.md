
### Strategies and Risks for Liquidity Providers

#### Introduction

Liquidity Providers are essential to decentralized prediction markets. Before forecasters can buy and sell outcome shares in a prediction market, markets are required to have liquidity.
The more liquidity is present in a market, the lesser the price impact when buying or selling outcome shares, and therefore more accurate is the forecast provided by that market.

**Benefits of Adding Liquidity:**
- Liquidity Providers can earn a Liquidity Providers Fee from every buy/sell transaction. By default, this fee is set to 2%, but the Market Creator can set it to 0% or 5%.
- The top Liquidity Providers are eligible for weekly rewards through the Protocol Incentives program.

**Risks of Providing Liquidity:**
- Risk associated with receiving outcome shares, the value of which fluctuates, as part of the total stake when adding or removing liquidity to and from a market.
- Risk of near-total loss, as ultimately the value of the shares of one of the outcomes will go to 0 after the market resolves.
- When a market’s Liquidity Provider Fees are set to 0%, a Liquidity Provider will have an even smaller chance of offsetting this risk.

The following sections will help better understand the risks and what strategies to adopt to increase the likelihood of being a successful Liquidity Provider.

#### Introduction to the Liquidity Mechanism

The Polkamarkets Protocol uses an Automated Market Maker (AMM) system adapted to the Prediction Markets use case. As with other AMM-powered systems, such as Uniswap or other DEXes, Liquidity Providers who use the Polkamarkets Protocol must implement strategies to deal with the risk of loss. 
Due to the zero-sum nature of prediction markets, the risk is greater than that incurred with other AMMs, as you’re risking near-total loss, rather than impermanent loss.

At the moment of market creation, the initial Liquidity Provider’s stake is converted to liquidity shares. 
If the price of all outcomes in the market is equal, the Liquidity Provider receives 100% of all Liquidity Pool Shares. The initial Liquidity Provider only receives liquidity shares in return for their liquidity, and does not receive any outcome shares. This is the case anytime that the price of both outcomes is equal. In this scenario, removing liquidity also returns 100% of the funds put in as liquidity.

When the price of the outcomes is unequal:
- When adding liquidity to the market, the Liquidity Provider will receive a portion of their stake in liquidity shares, and another portion in shares of all outcomes, except for the least likely outcome at that moment (i.e., the outcome with the lowest price).
- When removing liquidity, they will receive a portion of their stake as shares of all outcomes except for the most likely outcome (i.e., the outcome with the highest price).

#### The Best Moments to Add Liquidity to a Market

1. **At Market Creation:**
   - Liquidity Providers only receive shares of the Liquidity Pool and are not directly exposed to the variation of Outcome prices.

2. **When the Most Likely Outcome's Price is Not Close to 1:**
   - Liquidity Providers believe that the most likely Outcome will be the winning Outcome.
   - They want to maximize the earning potential of the Outcome shares that they receive.

**Rule of Thumb:**
- Only add liquidity when the current most likely Outcome is believed to be the winning outcome and is underpriced (i.e., its price will increase over time).

**Worst Moments to Add Liquidity:**
- When the most likely outcome is overpriced (i.e., its price is likely to decrease over time).
- When the incoming trading volume on a market will be too low to compensate for the risks.

#### The Best Moments to Remove Liquidity from a Market

**Rule of Thumb:**
- Always remove liquidity before the market closes if the outcome prices are uneven (almost always the case).
- Sell shares of the least likely outcomes, which are received when removing liquidity, while the market is still open for trades.

Consider the outcome prices and how they will evolve:
- If you think the most likely outcome is overpriced, sell shares, remove liquidity, and hold on to the shares of least likely outcomes.
- If you think the most likely outcome is underpriced, consider increasing your liquidity position or position in that outcome.

#### Benefiting from Volume

For liquidity provisioning to be more beneficial, the market must have a non-zero Liquidity Provider Fee and several times more trading volume than it has liquidity.

- The more buy and sell transactions happen on the market, and the higher the Fee, the more rewards are earned by the Liquidity Providers.
- Market Creators and Liquidity Providers should actively promote their markets to attract more forecasters and generate high trading volume.

**Example:**

The following graph shows the return on investment (ROI) of providing liquidity given different trading volume scenarios. The data assumes that:
- Liquidity is provided at the time of market creation, when the outcome prices are even (0.5 for outcome A and 0.5 for outcome B)
- The fee awarded to liquidity providers is 2%

![ROI Graph](link-to-graph)

**Key Points:**
- If the final price of the winning outcome is 0.5, the liquidity provider will always take a 2% profit if the trading volume is at least identical to the amount of liquidity added.
- If the price of the winning outcome is 0.99, the initial liquidity provider will only reach break-even (0.05% profitability) if the trading volume in the market is 45x greater than the market liquidity.

These extreme cases are rare. The average and median closing prices of the most likely outcome tend to be between 0.6 and 0.8 in most markets.

**Volume-to-Liquidity Ratio:**
- If liquidity is added when outcome prices are closer to closing prices, the ratio becomes less demanding.
- A higher fee reduces the volume-to-liquidity ratio required to achieve profitability.

For example, if the fee is set to 5% instead of 2%, the ratio of the extreme case where the most likely outcome is 0.99 is reduced to 18x, instead of 45x.
