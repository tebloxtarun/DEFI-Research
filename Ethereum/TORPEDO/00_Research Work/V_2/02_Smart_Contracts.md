

### UniswapV2Factory.sol

| Functionality              | Description                                                                                           | Functions                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Creating Liquidity Pairs   | Allows the creation of new trading pairs for ERC-20 tokens, ensuring no duplicates and proper initialization. | `createPair(address tokenA, address tokenB) external returns (address pair)`                              |
| Retrieving Pair Information| Provides functions to retrieve the address of existing pairs and list all pairs.                      | `getPair(address tokenA, address tokenB) external view returns (address pair)`                            |
|                            |                                                                                                       | `allPairs(uint index) external view returns (address pair)`                                               |
|                            |                                                                                                       | `allPairsLength() external view returns (uint)`                                                           |
| Managing Fees              | Enables configuration of fee addresses to collect protocol fees, ensuring only authorized updates.    | `setFeeTo(address) external`                                                                              |
|                            |                                                                                                       | `setFeeToSetter(address) external`                                                                        |
|                            |                                                                                                       | `feeTo() external view returns (address)`                                                                 |
|                            |                                                                                                       | `feeToSetter() external view returns (address)`                                                           |
| Transparency and Traceability| Emits events to track the creation of new pairs, enhancing transparency.                             | `event PairCreated(address indexed token0, address indexed token1, address pair, uint)`                   |

### UniswapV2ERC20.sol

| Functionality              | Description                                                                                           | Functions                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Token Standard Implementation| Implements the ERC-20 token standard, including essential functions like balance, transfer, approve, allowance. | `balanceOf(address owner) external view returns (uint)`                                                   |
|                            |                                                                                                       | `transfer(address to, uint value) external returns (bool)`                                                |
|                            |                                                                                                       | `approve(address spender, uint value) external returns (bool)`                                            |
|                            |                                                                                                       | `allowance(address owner, address spender) external view returns (uint)`                                  |
|                            |                                                                                                       | `transferFrom(address from, address to, uint value) external returns (bool)`                               |
| Permit Functionality       | Allows token approvals via signatures, enabling gasless transactions for the token holder.            | `permit(address owner, address spender, uint value, uint deadline, uint8 v, bytes32 r, bytes32 s) external`|
| Minting Tokens             | Internal function to mint new tokens and increase the total supply.                                   | `_mint(address to, uint value) internal`                                                                  |
| Burning Tokens             | Internal function to burn tokens and decrease the total supply.                                       | `_burn(address from, uint value) internal`                                                                |
| Approval and Transfer      | Handles approval and transfer of tokens, ensuring proper allowance checks and updating balances accordingly. | `approve`, `_approve`, `transfer`, `_transfer`, `transferFrom`                                            |
| Domain Separator and Permit Typehash | Implements EIP-712 compliant domain separator and permit typehash for secure off-chain signatures. | `DOMAIN_SEPARATOR() external view returns (bytes32)`                                                      |
|                            |                                                                                                       | `PERMIT_TYPEHASH() external pure returns (bytes32)`                                                       |
|                            |                                                                                                       | `nonces(address owner) external view returns (uint)`                                                      |

### UniswapV2Pair.sol

| Functionality              | Description                                                                                           | Functions                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Pair Initialization        | Initializes the pair contract with two ERC-20 tokens.                                                 | `initialize(address _token0, address _token1) external`                                                   |
| Liquidity Management       | Handles the addition and removal of liquidity from the pair, minting and burning liquidity tokens accordingly. | `mint(address to) external returns (uint liquidity)`                                                      |
|                            |                                                                                                       | `burn(address to) external returns (uint amount0, uint amount1)`                                          |
| Swapping Tokens            | Enables token swapping within the pair, ensuring that the invariant is maintained and handling token transfers. | `swap(uint amount0Out, uint amount1Out, address to, bytes calldata data) external`                        |
| Reserves Management        | Manages the reserves of the two tokens in the pair, ensuring they are kept in sync with the contract's balance. | `getReserves() external view returns (uint112 reserve0, uint112 reserve1, uint32 blockTimestampLast)`     |
|                            |                                                                                                       | `_update(uint balance0, uint balance1, uint112 _reserve0, uint112 _reserve1) private`                     |
|                            |                                                                                                       | `sync() external`                                                                                         |
| Fee Calculation and Distribution | Calculates and mints fees for the protocol, distributing them to the `feeTo` address if fees are enabled. | `_mintFee(uint112 _reserve0, uint112 _reserve1) private returns (bool feeOn)`                             |
| Event Emission             | Emits events for key actions within the pair contract, providing transparency and traceability of operations. | `Mint`, `Burn`, `Swap`, `Sync`                                                                            |
| Internal Safety and Transfer Functions | Ensures safe transfer of tokens, and allows for excess tokens to be skimmed to a specified address. | `_safeTransfer(address token, address to, uint value) private`                                            |
|                            |                                                                                                       | `skim(address to) external`                                                                               |

