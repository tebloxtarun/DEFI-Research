# Introduction

Before we dive into how outcome prices were programmed to be determined on the Torpedo Protocol, you should bear in mind the following facts:

- Whenever you’re trading, you’re effectively buying and selling shares of an outcome at the current price.
- An outcome is always guaranteed a price between 0 and 1 unit in the market’s token (which can be any ERC-20 token).
- The sum of the price of all outcomes is always 1.
- After the market resolves, the winning outcome will have a price value of 1, while the price of all the losing outcomes will be 0.


### Price Calculation at the Time of a Trade

When a trade happens, a number of shares of a particular outcome is bought or sold, which means that shares are added or removed from that outcome's pool, and that shares are added to or removed from the prediction market participant's balance.

As the distribution of shares available in the overall pool changes, so changes the price of each outcome. Let’s take a detailed look at how the prices are impacted when a participant decides to buy shares of an outcome.

#### In a Binary Outcome Market

1. **Trade Example:**
   - Bob decides to buy 300 USDC worth of shares of Outcome A in the market created by Alice.
   - Bob pays a 2% trading fee, so he adds 294 USDC to the market.

2. **Updating Shares:**
   - 294 shares are added to both Outcome A and Outcome B pools.
   - The new shares are:
     - Outcome A: 1294 shares
     - Outcome B: 1294 shares

3. **Recalculating Shares:**
   - Using the formula: 
     \( \text{SharesOutcomeA} = \frac{\text{SharesLiquidityPool}^2}{\text{SharesOutcomeB}} \)
   - Outcome A recalculated to 773 shares.

4. **Bob's Purchase:**
   - Bob effectively buys \( 1294 - 773 = 521 \) shares of Outcome A.

5. **Price Impact:**
   - New price of Outcome A: \( \frac{1294}{1294 + 773} = 0.63 \)
   - New price of Outcome B: \( \frac{773}{1294 + 773} = 0.37 \)

#### In a Multiple Outcome Market

1. **Trade Example:**
   - Dylan decides to buy 300 USDC worth of shares of Outcome A in the multiple outcome market created by Charlie.
   - Dylan pays a 2% trading fee, so he adds 294 USDC to the market.

2. **Updating Shares:**
   - 294 shares are added to Outcome A, B, C, and D pools.
   - New shares are:
     - Outcome A: 1294 shares
     - Outcome B: 1294 shares
     - Outcome C: 1294 shares
     - Outcome D: 1294 shares

3. **Recalculating Shares:**
   - Using the formula:
     \( \text{SharesOutcomeA} = \frac{\text{SharesLiquidityPool}^4}{\text{SharesOutcomeB} \times \text{SharesOutcomeC} \times \text{SharesOutcomeD}} \)
   - Outcome A recalculated to 461.53 shares.

4. **Dylan's Purchase:**
   - Dylan effectively buys \( 1294 - 461.53 = 832.47 \) shares of Outcome A.

5. **Price Impact:**
   - Price weights and new prices calculated:
     - Outcome A: \( \frac{2166720184}{4485127525.24} \approx 0.48 \)
     - Outcome B, C, D: \( \frac{772802447.08}{4485127525.24} \approx 0.17 \)

### Summary Table:

| Property                   | Description                                                                                                                                                                                                                                 | Example                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| **Trade Example**          | The participant buys a specified amount of shares for an outcome, paying a trading fee.                                                                                                                                                       | Bob buys 300 USDC worth of shares for Outcome A.                                           |
| **Updating Shares**        | Shares are added to each outcome pool after the trade.                                                                                                                                                                                       | Outcome A = 1294 shares, Outcome B = 1294 shares                                           |
| **Recalculating Shares**   | Recalculates the number of shares in the pools using a formula.                                                                                                                                                                               | Outcome A recalculated to 773 shares.                                                      |
| **Participant's Purchase** | The participant buys the difference between the total shares and recalculated shares.                                                                                                                                                         | Bob buys \( 1294 - 773 = 521 \) shares of Outcome A.                                       |
| **Price Impact**           | New prices of outcomes are calculated after the trade.                                                                                                                                                                                        | Outcome A price: \( \frac{1294}{1294 + 773} = 0.63 \), Outcome B price: \( \frac{773}{1294 + 773} = 0.37 \) |
| **Multiple Outcome Market**| Similar steps for multiple outcome markets, considering multiple outcomes.                                                                                                                                                                    | Outcome A recalculated to 461.53 shares, price recalculated for all outcomes.              |





 
​
