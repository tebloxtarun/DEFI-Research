
# Uses of the Contracts

## UniswapFactoryInterface (Factory Contract)
1. **Create New Exchange**
   - Facilitates the creation of new exchanges for different ERC-20 tokens.
   
2. **Track Exchange and Token Information**
   - Maintains a registry of exchanges and their associated ERC-20 tokens.
   
3. **Initialize Factory**
   - Sets up the factory with the necessary exchange template to create new exchanges.

## UniswapExchangeInterface (Exchange Contract)
1. **Liquidity Management**
   - Allows users to add and remove liquidity to/from the exchange.
   
2. **ETH to Token Trading**
   - Facilitates the trading of ETH for ERC-20 tokens.
   
3. **Token to ETH Trading**
   - Facilitates the trading of ERC-20 tokens for ETH.
   
4. **Token to Token Trading**
   - Facilitates the trading of one ERC-20 token for another ERC-20 token.
   
5. **Token to Custom Pool Trading**
   - Facilitates the trading of ERC-20 tokens for tokens from another exchange pool.
   
6. **Get Pricing Information**
   - Provides current pricing information for ETH/token and token/ETH trades.

## ERC20Interface (ERC-20 Token Contract)
1. **Total Supply Management**
   - Keeps track of the total supply of the ERC-20 token.
   
2. **Balance Tracking**
   - Allows users to check the balance of tokens held by different addresses.
   
3. **Allowance Management**
   - Manages and tracks allowances set by token holders for third-party spenders.
   
4. **Token Transfer**
   - Facilitates the transfer of tokens between addresses.
   
5. **Approval and Transfer on Behalf**
   - Allows token holders to approve third parties to transfer tokens on their behalf.
