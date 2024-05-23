### Overview of Uniswap V1 Functionality

**1. Structure and Creation**
- **ETH-ERC20 Exchange Contracts**: Each ERC20 token has a unique exchange contract.
- **Uniswap Factory Contract**: Anyone can create an exchange for a token using this contract, which serves as a public registry.

**2. Liquidity Provision**
- **Liquidity Pools**: Reserves of ETH and the associated ERC20 token.
- **Becoming a Liquidity Provider**: Deposit equivalent value of ETH and the ERC20 token.
- **Pool Tokens**: ERC20 tokens that track contributions, minted when liquidity is added, and burned when liquidity is withdrawn.

**3. Trading Mechanism**
- **Automated Market Maker**: Allows swapping between ETH and ERC20 tokens.
- **Constant Product Formula**: Sets exchange rates based on reserve sizes and trade amounts.
- **Price Slippage**: Larger trades relative to reserves cause more slippage.

**4. Fee Structure**
- **Liquidity Provider Fee**: 0.30% fee on each trade, added to reserves, collected by burning pool tokens.
- **Arbitrage Opportunities**: Encourage steady transaction flow and fee generation.

**5. On-Chain Transactions**
- **Price Fluctuation Boundaries**: Limit orders can be set to bound price changes.
- **Transaction Deadlines**: Orders can be canceled if not executed within a set timeframe.

**6. Single Exchange Per Token**
- **Liquidity Pool Consolidation**: Encourages pooling liquidity into a single reserve for efficiency.

**7. Custom Pools**
- **Custom Pool Features**: Can have fund managers, alternate pricing, no fees, etc.
- **Interaction with Custom Pools**: Must implement Uniswap interface and use ETH as an intermediary.
- **Safety**: Custom pools may lack the safety of public pools; recommended to use audited, open-source contracts.

**8. Upgrades and Versions**
- **Censorship Resistance and Decentralization**: Upgrading is complex.
- **New Versions**: Liquidity providers can choose to switch; new versions aim for backward compatibility.
