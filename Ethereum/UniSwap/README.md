### Feature2: Constant Product Market Maker Model

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Swap UI | Frontend Interface | Captures user input | User navigates to the token swap module and selects tokens. | User selects to swap ETH for DAI and specifies the amount of ETH to swap. |
| 2    | Frontend Sends Request to Backend Service | Frontend Interface → Backend Services | Communicates user's request | User enters the swap details and submits the request. | The frontend sends a request containing the swap details to the backend service responsible for handling swaps. |
| 3    | Backend Validates and Prepares Transaction | Backend Services | Ensures request validity | Validates the swap request and prepares transaction data. | Checks if the user has enough ETH and if the ETH/DAI pair exists. |
| 4    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates token swap | Sends the prepared transaction data to the smart contract. | Sends swap details to the smart contract handling the liquidity pool. |
| 5    | Smart Contract Executes Swap | Smart Contracts | Performs token swap | Executes the token swap using the CPMM formula. | Adjusts the balances of ETH and DAI in the liquidity pool, ensuring \(x \cdot y = k\). |
| 6    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 7    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the swap details and outcome. | Emits events such as SwapExecuted with details of the tokens swapped and amounts. |
| 8    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed swap. |
| 9    | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process. |


### Feature 3: On-Chain Liquidity Pools

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Liquidity UI | Frontend Interface | Captures user input | User navigates to the liquidity provision module and selects tokens to provide. | User selects to provide ETH and DAI and specifies the amounts. |
| 2    | Frontend Sends Request to Backend Service | Frontend Interface → Backend Services | Communicates user's request | User enters the details and submits the request. | The frontend sends a request containing the liquidity provision details to the backend service. |
| 3    | Backend Validates and Prepares Transaction | Backend Services | Ensures request validity | Validates the request and prepares transaction data. | Checks if the user has enough tokens and if the pool exists. |
| 4    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates liquidity provision | Sends the prepared transaction data to the smart contract. | Sends liquidity details to the smart contract handling the liquidity pool. |
| 5    | Smart Contract Executes Provision | Smart Contracts | Performs liquidity provision | Executes the transaction, adding the tokens to the pool. | Adjusts the balances of ETH and DAI in the pool and issues liquidity tokens. |
| 6    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated pool balances are recorded. |
| 7    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the provision details and outcome. | Emits events such as LiquidityAdded with details of the tokens provided and amounts. |
| 8    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed provision. |
| 9    | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the provision process. |

### Feature 4: Decentralized Token Swaps

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Swap UI | Frontend Interface | Captures user input | User navigates to the token swap module and selects tokens. | User selects to swap ETH for DAI and specifies the amount of ETH to swap. |
| 2    | Frontend Sends Swap Request | Frontend Interface → Backend Services | Communicates user's request | User enters the swap details and submits the request. | The frontend sends a request containing the swap details to the backend service. |
| 3    | Backend Validates Request | Backend Services | Ensures request validity | Validates the swap request, checking for sufficient balance and valid token pairs. | Checks if the user has enough ETH in their wallet and if the ETH/DAI pair exists. |
| 4    | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data, including necessary parameters for the smart contract call. | Calculates the output amount of DAI based on the CPMM formula. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates token swap | Sends the prepared transaction data to the smart contract. | Sends swap details to the smart contract handling the liquidity pool. |
| 6    | Smart Contract Executes Swap | Smart Contracts | Performs token swap | Uses the CPMM formula to execute the swap. | Adjusts the balances of ETH and DAI in the liquidity pool. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the swap details and outcome. | Emits events such as SwapExecuted with details of the tokens swapped and amounts. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed swap. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process. |

### Feature 5: Permissionless Listing

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Listing UI | Frontend Interface | Captures user input | User navigates to the token listing module and enters token details. | User specifies the new token's details for listing. |
| 2    | Frontend Sends Listing Request | Frontend Interface → Backend Services | Communicates user's request | User submits the token listing request. | The frontend sends a request containing the token details to the backend service. |
| 3    | Backend Validates Request | Backend Services | Ensures request validity | Validates the listing request, checking the token details and parameters. | Checks if the token details are correct and valid for listing. |
| 4    | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data, including necessary parameters for the smart contract call. | Prepares data for creating a new liquidity pool for the token. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates token listing | Sends the prepared transaction data to the smart contract. | Sends listing details to the smart contract handling new listings. |
| 6    | Smart Contract Creates Pool | Smart Contracts | Creates new liquidity pool | Executes the transaction, creating a new liquidity pool for the token. | A new liquidity pool for the token is created and initialized. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and the new pool is recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the listing details and outcome. | Emits events such as TokenListed with details of the new token listing. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed listing. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the listing process. |

### Feature 6: No Order Book

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Real-Time Prices | Frontend Interface | Displays real-time prices | User navigates to the swap interface to see token prices. | User views the current price of ETH in DAI. |
| 2    | Frontend Fetches Data from Backend | Frontend Interface → Backend Services | Retrieves price data | Frontend requests real-time price data from the backend. | The frontend sends a request for current token prices to the backend service. |
| 3    | Backend Fetches Liquidity Data | Backend Services | Retrieves liquidity data | Backend fetches liquidity data from the smart contracts. | Backend requests the current liquidity pool state from the smart contract. |
| 4    | Backend Prepares Price Data | Backend Services | Formats price data | Formats the liquidity data into user-friendly price information. | Calculates the current price of ETH based on liquidity pool data. |
| 5    | Backend Sends Price Data to Frontend | Backend Services → Frontend Interface | Provides price data | Sends the formatted price data to the frontend interface. | Backend sends the calculated price of ETH to the frontend. |
| 6    | Frontend Updates Real-Time Prices | Frontend Interface | Updates UI with prices | Displays the updated real-time prices on the user interface. | Frontend shows the current price of ETH in the swap interface. |
| 7    | User Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process. |

### Feature 7: Gas Efficiency

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Optimized Submission | Frontend Interface | Optimizes transaction submission | User initiates a token swap with optimized gas settings. | User selects to swap ETH for DAI and specifies the amount of ETH to swap. |
| 2    | Frontend Sends Optimized Request | Frontend Interface → Backend Services | Communicates user's request | User submits the optimized swap request. | The frontend sends a request containing the swap details to the backend service. |
| 3    | Backend Validates Request | Backend Services | Ensures request validity | Validates the swap request and checks for gas optimizations. | Checks if the user has enough ETH in their wallet and if the ETH/DAI pair exists. |
| 4    | Backend Prepares Optimized Transaction Data | Backend Services | Formats data for smart