
### Removing Liquidity from Polkamarkets

Removing liquidity from a market has the same constraints, and the opposite effect, of adding liquidity to a market. 
As the price of the outcomes cannot be impacted by the rebalancing of the pools, the Liquidity Provider will receive shares of all the outcomes except for the most likely (i.e. most expensive) outcome (instead of all but the least likely) when removing liquidity from a market.
When the prices of all outcomes are equal, removing liquidity will not result in the Liquidity Provider receiving any outcome shares.

### Removing Liquidity while the Market is Open

As described in Strategies and Risks for Liquidity Providers, a Liquidity Provider should always aim to remove their liquidity before a market closes. Let's look at a couple of examples.

#### Example: Removing Liquidity from a Market with Unequal Binary Outcome Prices

- **Initial Market:**
  - Liquidity Value: $5600 USDC
  - Outcome A Shares: 3578.97 (Price: 0.71)
  - Outcome B Shares: 8762.30 (Price: 0.29)
  - Bob's Portfolio:
    - Liquidity Shares: 782.88
    - Outcome A Shares: 387.10

- **Action:**
  - Bob removes his 782.88 Liquidity Pool shares.
  - Value of Bob's LP shares:
    Value = (LowestOutcomeShares * LiquidityShares) / MarketLiquidity
    Value = (8762.30 * 782.88) / 5600 = 500.34 USDC

- **Temporary Market Status:**
  - Liquidity Value: $5099.66 USDC
  - Outcome A Shares: 3078.629
  - Outcome B Shares: 8261.962

- **Rebalancing:**
  - Recalculate Outcome B shares:
    SharesOutcomeB = (SharesOutcomeA * PriceOutcomeA) / PriceOutcomeB
    SharesOutcomeB = (3078.629 * 0.71) / 0.29 = 7537.33
  - Bob gets Outcome B shares:
    SharesReceived = 8261.962 - 7537.33 = 724.630

- **Final Market Status:**
  - Outcome A Shares: 3078.629
  - Outcome B Shares: 7537.33
  - Liquidity Value: (3078.629 * 7537.33) = 4817.12 USDC

- **Bob's Portfolio after Removing Liquidity:**
  - Outcome A Shares: 387.10
  - Outcome B Shares: 724.630
  - Total Value: $477.7374 USDC

#### Example: Removing Liquidity from a Market with Multiple Outcomes

- **Initial Market:**
  - Outcome A Shares: 812.46 (Price: 0.48)
  - Outcome B, C, D Shares: 2294 each (Price: 0.17)
  - Liquidity Shares: 1769.68

- **Action:**
  - Charlie removes 300 Liquidity Pool shares.
  - Value of Charlie's LP shares:
    Value = (LowestOutcomeShares * LiquidityShares) / MarketLiquidity
    Value = (2294 * 300) / 1769.68 = 231.43 USDC

- **Temporary Market Status:**
  - Outcome A Shares: 581.03
  - Outcome B, C, D Shares: 2062.57 each

- **Rebalancing:**
  - Recalculate Outcome B shares:
    SharesOutcomeB = (SharesOutcomeA * PriceOutcomeA) / PriceOutcomeB
    SharesOutcomeB = (581.03 * 0.48) / 0.17 = 1640.55
  - Charlie gets shares of B, C, D:
    SharesReceived = 2062.57 - 1640.55 = 422.02 each

- **Final Market Status:**
  - Outcome A Shares: 581.03
  - Outcome B, C, D Shares: 1640.55 each
  - Liquidity Value: (581.03 * 1640.55 * 1640.55 * 1640.55) / 4 = 1265.59

- **Charlie's Portfolio after Removing Liquidity:**
  - Liquidity Shares: 700
  - Outcome B, C, D Shares: 422.02 each

### Removing Liquidity after Market Resolution

Removing liquidity after a market is resolved is possible but not ideal. The value of a liquidity share is calculated as follows:
LiquiditySharePrice = MarketLiquidity / NumberOfSharesOfTheWinningOutcome

For example, in a market with $1000 USDC in liquidity that resolves to Outcome A with 500 shares, a Liquidity Provider claiming back 300 Liquidity Pool shares will get:
300 * 500 / 1000 = 150 USDC

