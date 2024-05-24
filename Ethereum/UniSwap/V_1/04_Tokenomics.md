### Uniswap Tokenomics Overview

1. **Exchange Pools**:
   - Each ERC-20 token has a dedicated exchange holding reserves of ETH and the token.
   - Liquidity providers add assets to these pools.

2. **Liquidity Provision**:
   - Providers earn a 0.3% fee on trades.
   - Fees are distributed proportionally among liquidity providers.

3. **Automated Market Making**:
   - Uses the constant product formula \( x \cdot y = k \).
   - Prices adjust automatically based on reserves.

4. **Trading Mechanism**:
   - Users trade directly against the reserves.
   - No order matching needed; prices are algorithmically determined.

5. **ETH as Common Pair**:
   - ETH is the intermediary for ERC-20 to ERC-20 trades.
   - Trades involve two steps: ERC-20 to ETH, then ETH to ERC-20.

6. **Pricing Calculations**:
   - **Sell Orders**: Output amount is calculated with:
     \[
     \text{outputAmount} = \frac{\text{inputAmount} \cdot \text{outputReserve} \cdot 997}{\text{inputReserve} \cdot 1000 + \text{inputAmount} \cdot 997}
     \]
   - **Buy Orders**: Input cost is calculated with:
     \[
     \text{inputAmount} = \frac{\text{outputAmount} \cdot \text{inputReserve} \cdot 1000}{(\text{outputReserve} - \text{outputAmount}) \cdot 997} + 1
     \]

7. **ERC-20 to ERC-20 Trading**:
   - Involves converting TokenA to ETH, then ETH to TokenB.
   - Combined fee:
     \[
     \text{combinedFee} = \text{inputAmountA} \cdot 0.00591
     \]

8. **Exchange Rates**:
   - Determined by:
     \[
     \text{rate} = \frac{\text{outputAmount}}{\text{inputAmount}}
     \]

9. **Deadlines**:
   - Set to prevent indefinite holding by miners.
   - Calculated from the latest block timestamp.

10. **Recipients**:
    - Output tokens can be transferred to a different address, allowing for versatile payment scenarios.
