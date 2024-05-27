
### Functions of `IUniswapV2Pair`

| Serial No. | Interface      | Function Name              | Input Parameters                                                         | Output                      | Description                                                                                  |
|------------|----------------|----------------------------|--------------------------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------|
| 1          | IUniswapV2Pair | `name`                     | None                                                                     | `string memory`             | Returns the name of the token.                                                               |
| 2          | IUniswapV2Pair | `symbol`                   | None                                                                     | `string memory`             | Returns the symbol of the token.                                                             |
| 3          | IUniswapV2Pair | `decimals`                 | None                                                                     | `uint8`                     | Returns the number of decimals the token uses.                                               |
| 4          | IUniswapV2Pair | `totalSupply`              | None                                                                     | `uint`                      | Returns the total supply of tokens.                                                          |
| 5          | IUniswapV2Pair | `balanceOf`                | `address owner`                                                          | `uint`                      | Returns the balance of tokens for the specified address.                                     |
| 6          | IUniswapV2Pair | `allowance`                | `address owner`, `address spender`                                       | `uint`                      | Returns the remaining number of tokens that spender is allowed to spend on behalf of owner. |
| 7          | IUniswapV2Pair | `approve`                  | `address spender`, `uint value`                                          | `bool`                      | Approves the spender to spend up to value tokens.                                            |
| 8          | IUniswapV2Pair | `transfer`                 | `address to`, `uint value`                                               | `bool`                      | Transfers value tokens to the specified address.                                             |
| 9          | IUniswapV2Pair | `transferFrom`             | `address from`, `address to`, `uint value`                               | `bool`                      | Transfers value tokens from one address to another using the allowance mechanism.            |
| 10         | IUniswapV2Pair | `DOMAIN_SEPARATOR`         | None                                                                     | `bytes32`                   | Returns the domain separator for EIP-712.                                                    |
| 11         | IUniswapV2Pair | `PERMIT_TYPEHASH`          | None                                                                     | `bytes32`                   | Returns the type hash for permit.                                                            |
| 12         | IUniswapV2Pair | `nonces`                   | `address owner`                                                          | `uint`                      | Returns the current nonce for the owner.                                                     |
| 13         | IUniswapV2Pair | `permit`                   | `address owner`, `address spender`, `uint value`, `uint deadline`, `uint8 v`, `bytes32 r`, `bytes32 s` | None                        | Approves spending via signature.                                                             |
| 14         | IUniswapV2Pair | `MINIMUM_LIQUIDITY`        | None                                                                     | `uint`                      | Returns the minimum liquidity constant.                                                      |
| 15         | IUniswapV2Pair | `factory`                  | None                                                                     | `address`                   | Returns the factory address.                                                                 |
| 16         | IUniswapV2Pair | `token0`                   | None                                                                     | `address`                   | Returns the address of the first token.                                                      |
| 17         | IUniswapV2Pair | `token1`                   | None                                                                     | `address`                   | Returns the address of the second token.                                                     |
| 18         | IUniswapV2Pair | `getReserves`              | None                                                                     | `uint112 reserve0`, `uint112 reserve1`, `uint32 blockTimestampLast` | Returns the current reserves and last block timestamp.                                      |
| 19         | IUniswapV2Pair | `price0CumulativeLast`     | None                                                                     | `uint`                      | Returns the last cumulative price for token0.                                                |
| 20         | IUniswapV2Pair | `price1CumulativeLast`     | None                                                                     | `uint`                      | Returns the last cumulative price for token1.                                                |
| 21         | IUniswapV2Pair | `kLast`                    | None                                                                     | `uint`                      | Returns the last k value.                                                                    |
| 22         | IUniswapV2Pair | `mint`                     | `address to`                                                             | `uint liquidity`            | Mints liquidity tokens to the specified address.                                             |
| 23         | IUniswapV2Pair | `burn`                     | `address to`                                                             | `uint amount0`, `uint amount1` | Burns liquidity tokens and sends the underlying assets to the specified address.             |
| 24         | IUniswapV2Pair | `swap`                     | `uint amount0Out`, `uint amount1Out`, `address to`, `bytes calldata data` | None                        | Swaps tokens, supporting flash swaps.                                                        |
| 25         | IUniswapV2Pair | `skim`                     | `address to`                                                             | None                        | Sends excess tokens to the specified address.                                                |
| 26         | IUniswapV2Pair | `sync`                     | None                                                                     | None                        | Updates the reserves to match the current balances of the contract.                         |
| 27         | IUniswapV2Pair | `initialize`               | `address token0`, `address token1`                                       | None                        | Initializes the pair with the two tokens.                                                    |

### Functions of `IERC20`

| Serial No. | Interface | Function Name              | Input Parameters                         | Output  | Description                                                                 |
|------------|-----------|----------------------------|------------------------------------------|---------|-----------------------------------------------------------------------------|
| 28         | IERC20    | `totalSupply`              | None                                     | `uint`  | Returns the total supply of tokens.                                         |
| 29         | IERC20    | `balanceOf`                | `address owner`                          | `uint`  | Returns the balance of tokens for a specific address.                       |
| 30         | IERC20    | `allowance`                | `address owner`, `address spender`       | `uint`  | Returns the remaining number of tokens that spender is allowed to spend.    |
| 31         | IERC20    | `approve`                  | `address spender`, `uint value`          | `bool`  | Approves the spender to spend up to value tokens.                           |
| 32         | IERC20    | `transfer`                 | `address to`, `uint value`               | `bool`  | Transfers value tokens to the specified address.                            |
| 33         | IERC20    | `transferFrom`             | `address from`, `address to`, `uint value` | `bool` | Transfers value tokens from one address to another using the allowance.     |

### Functions of `IUniswapV2Factory`

| Serial No. | Interface          | Function Name    | Input Parameters                   | Output    | Description                                                      |
|------------|--------------------|------------------|------------------------------------|-----------|------------------------------------------------------------------|
| 34         | IUniswapV2Factory  | `feeTo`          | None                               | `address` | Returns the address to which fees are sent.                      |
| 35         | IUniswapV2Factory  | `feeToSetter`    | None                               | `address` | Returns the address that can set the fee recipient.              |
| 36         | IUniswapV2Factory  | `getPair`        | `address tokenA`, `address tokenB` | `address` | Returns the address of the pair contract for the specified tokens.|
| 37         | IUniswapV2Factory  | `allPairs`       | `uint`                             | `address` | Returns the address of the pair contract at the specified index. |
| 38         | IUniswapV2Factory  | `allPairsLength` | None                               | `uint`    | Returns the total number of pairs.                               |
| 39         | IUniswapV2Factory  | `createPair`     | `address tokenA`, `address tokenB` | `address` | Creates a new pair for the specified tokens.                     |
| 40         | IUniswapV2Factory  | `setFeeTo`       | `address`                          | None      | Sets the address to which fees are sent.                         |
| 41         | IUniswapV2Factory  | `setFeeToSetter` | `address`                          | None      | Sets the address that can update the fee recipient.              |

### Functions of `IUniswapV2Callee`

| Serial No. | Interface        | Function Name   | Input Parameters                                                 | Output | Description                                                                         |
|------------|------------------|-----------------|------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------|
| 42         | IUniswapV2Callee | `uniswapV2Call` | `address sender`, `uint amount0`, `uint amount1`, `bytes calldata data` | None   | Called by the Uniswap V2 Pair contract during a swap to execute custom logic.       |
