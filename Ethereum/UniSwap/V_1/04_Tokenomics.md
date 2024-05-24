### Uniswap Tokenomics
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

![image](https://github.com/tebloxtarun/DEFI-Research/assets/170435024/c4ae43e7-3025-4a18-8b1d-095246fa383d)  
7. **ERC-20 to ERC-20 Trading**:
   - Involves converting TokenA to ETH, then ETH to TokenB.  
![image](https://github.com/tebloxtarun/DEFI-Research/assets/170435024/a72b5f18-8df8-4469-8a80-f24f24e95bdc)

8. **Exchange Rates**:
   - Determined by:  
![image](https://github.com/tebloxtarun/DEFI-Research/assets/170435024/7e80e35b-276b-4b2c-ac1e-c618b1c2d152)


9. **Deadlines**:
   - Set to prevent indefinite holding by miners.
   - Calculated from the latest block timestamp.

10. **Recipients**:
    - Output tokens can be transferred to a different address, allowing for versatile payment scenarios.
