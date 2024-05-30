
### Adding Liquidity to Polkamarkets

When a Liquidity Provider adds liquidity to an existing market, two main things happen:
1. The Liquidity Provider is assigned shares of the Liquidity Pool proportional to their contribution.
2. If the outcome prices are not equal, the Liquidity Provider will receive shares of all outcomes, except for the least likely (least expensive) outcome at the time of funding.

#### Logic

The Automated Market Maker (AMM) ensures balance between the Liquidity Pool shares and the Outcome Share Pools. When liquidity is added:
- If outcome shares are equal (prices are equal), the Liquidity Provider gets only Liquidity Pool shares.
- If outcome shares are unequal (prices are unequal), the Liquidity Provider gets shares from the most likely outcomes and not from the least likely ones to maintain balance.

### Examples

#### Example 1: Adding Liquidity with Equal Outcome Prices

- **Initial Market:**
  - Liquidity Value: $100 USDC
  - Outcome A Shares: 100
  - Outcome B Shares: 100
  - Outcome A Price: $0.5
  - Outcome B Price: $0.5
  - Alice holds 100 shares of the Liquidity Pool.

- **Action:**
  - Alice adds $1000 USDC in liquidity.

- **New Market Status:**
  - Liquidity Value: $1100 USDC
  - Outcome A Shares: 1100
  - Outcome B Shares: 1100
  - Outcome A Price: $0.5
  - Outcome B Price: $0.5
  - Alice receives 1000 shares of the Liquidity Pool, now holding 1100 shares.

#### Example 2: Adding Liquidity with Unequal Outcome Prices

- **Market After Trades:**
  - Liquidity Value: $1100 USDC
  - Outcome A Shares: 861.17
  - Outcome B Shares: 1405.07
  - Outcome A Price: $0.62
  - Outcome B Price: $0.38

- **Action:**
  - Bob adds $1000 USDC in liquidity.

- **Temporary Status:**
  - Liquidity Value: $2100 USDC
  - Outcome A Shares: 1861.17
  - Outcome B Shares: 2405.07

- **Rebalancing:**
  - Using the formula:
    SharesOutcomeA = (SharesOutcomeB * PriceOutcomeB) / PriceOutcomeA
    SharesOutcomeA = (2405.07 * 0.38) / 0.62 = 1474.07

- **Final Status:**
  - Outcome A Shares: 1474.07
  - Outcome B Shares: 2405.07
  - Liquidity Value: $1882.88
  - Bob gets:
    - Liquidity Shares: 1882.88 - 1000 = 882.88
    - Outcome A Shares: 1861.17 - 1474.07 = 387.10

### Adding Liquidity to a Multiple Outcome Market

#### Example 3: Adding Liquidity to a Market with Multiple Outcomes

- **Initial Market:**
  - Liquidity Shares: 1000
  - Outcome A Shares: 461.53 (Price: 0.48)
  - Outcome B Shares: 1294 (Price: 0.17)
  - Outcome C Shares: 1294 (Price: 0.17)
  - Outcome D Shares: 1294 (Price: 0.17)

- **Action:**
  - Dylan adds $1000 USDC in liquidity.

- **Temporary Status:**
  - Liquidity Shares: 2000
  - Outcome A Shares: 1461.53
  - Outcome B, C, D Shares: 2294 each

- **Rebalancing:**
  - Using the formula:
    SharesOutcomeA = (SharesLeastLikelyOutcome * PriceLeastLikelyOutcome) / PriceOutcomeA
    SharesOutcomeA = (2294 * 0.17) / 0.48 = 812.46

- **Final Status:**
  - Outcome A Shares: 812.46
  - Outcome B, C, D Shares: 2294 each
  - Liquidity Value: (812.46 * 2294 * 2294 * 2294) / 4 = 1769.68
  - Dylan gets:
    - Liquidity Shares: 1769.68 - 1000 = 769.68
    - Outcome A Shares: 1461.53 - 812.46 = 649.07

### Summary Table:

| Property                           | Description                                                                                                                      | Example                                                                                   |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| **Adding Liquidity (Equal Prices)**| Adding liquidity when outcome prices are equal, resulting in equal shares in each pool and no change in prices.                  | Alice adds $1000 USDC to the market with balanced prices, receiving Liquidity Pool shares.|
| **Adding Liquidity (Unequal Prices)**| Adding liquidity when outcome prices are unequal, resulting in rebalancing to maintain market balance and avoid price changes.  | Bob adds $1000 USDC, resulting in recalculated shares and prices.                         |
| **Rebalancing Formula (Binary)**   | Formula to recalculate shares when adding liquidity to maintain market balance.                                                   | SharesOutcomeA = (SharesOutcomeB * PriceOutcomeB) / PriceOutcomeA                         |
| **Adding Liquidity (Multiple Outcomes)**| Adding liquidity in a market with multiple outcomes, resulting in shares from all outcomes except the least likely one.          | Dylan adds $1000 USDC, getting shares of Outcome A and Liquidity Pool shares.             |
| **Rebalancing Formula (Multiple)** | Formula to recalculate shares in multiple outcome markets.                                                                        | SharesOutcomeA = (SharesLeastLikelyOutcome * PriceLeastLikelyOutcome) / PriceOutcomeA     |
