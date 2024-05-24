# BluePrint for Factory Contract  

```bash
contract UniswapFactoryInterface():
    # Create Exchange
    def createExchange(token: address) -> address: modifying
    # Public Variables
    def exchangeTemplate() -> address: constant
    def tokenCount() -> uint256: constant
    # Get Exchange and Token Info
    def getExchange(token_addr: address) -> address: constant
    def getToken(exchange: address) -> address: constant
    def getTokenWithId(token_id: uint256) -> address: constant
    # Initialize Factory
    def initializeFactory(template: address): modifying
```

### Uniswap factory contract functions:
| Function            | Parameter(s)                  | Returns            | Smart Contract Function                       | Web3 Call                                                    | Description                                                                       |
|---------------------|-------------------------------|--------------------|----------------------------------------------|--------------------------------------------------------------|-----------------------------------------------------------------------------------|
| initializeFactory   | `template` (address)          | N/A                | `initializeFactory(template: address)`       | `factoryContract.methods.initializeFactory(template).send()` | Initializes the factory with the given exchange template address.                |
| createExchange      | `token` (address)             | `address`          | `createExchange(token: address): address`    | `factoryContract.methods.createExchange(token).send()`       | Deploys an exchange contract for the given ERC20 token and returns its address.   |
| getExchange         | `token` (address)             | `address`          | `@constant getExchange(token: address): address` | `factoryContract.methods.getExchange(token).call()`          | Retrieves the address of the exchange contract associated with the given ERC20 token. |
| getToken            | `exchange` (address)          | `address`          | `@constant getToken(exchange: address): address` | `factoryContract.methods.getToken(exchange).call()`          | Retrieves the address of the ERC20 token associated with the given exchange contract. |
| getTokenWithId      | `token_id` (uint256)          | `address`          | `@constant getTokenWithId(token_id: uint256): address` | `factoryContract.methods.getTokenWithId(token_id).call()`    | Retrieves the address of the ERC20 token associated with the given Uniswap token ID. |

