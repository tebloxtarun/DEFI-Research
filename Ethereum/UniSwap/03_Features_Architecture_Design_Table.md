### Feature1: Modular Component Based Design

| Step | Action | Component | Description |
|------|--------|-----------|-------------|
| 1    | Design Modular UI Components | Frontend Interface | Design the user interface in a modular fashion, where each feature is a separate, independent module. |
| 2    | Develop Decoupled Microservices | Backend Services | Implement backend services as independent microservices, each handling a specific functionality. |
| 3    | Create Modular Smart Contracts | Smart Contracts | Write smart contracts in a modular way, where each contract handles a specific function or set of related functions. |
| 4    | Support Dynamic Updates | Blockchain Network | Ensure the blockchain network supports dynamic updates to smart contracts and modules without requiring a complete system overhaul. |
| 5    | Adapt Wallet Integrations | Wallet Integrations | Integrate with wallets to support the modular nature of the application, allowing users to interact with different modules seamlessly. |
| 6    | User Interaction with Modular UI | Frontend Interface | User navigates to the token swap module in the frontend interface, loading the relevant options and input fields. |
| 7    | Frontend Sends Request to Appropriate Microservice | Frontend Interface → Backend Services | The frontend interface sends the token swap request to the corresponding microservice. |
| 8    | Microservice Processes the Request | Backend Services | The token swap microservice validates the user request and prepares the transaction data. |
| 9    | Microservice Calls the Smart Contract | Backend Services → Smart Contracts | The microservice sends the formatted transaction data to the smart contract handling token swaps. |
| 10   | Smart Contract Executes the Transaction | Smart Contracts → Blockchain Network | The smart contract performs the token swap according to the predefined logic. |
| 11   | Blockchain Confirms the Transaction | Blockchain Network | The blockchain network validates and confirms the transaction. |
| 12   | Microservice Updates the Frontend | Backend Services → Frontend Interface | The microservice retrieves the transaction status and updates the frontend interface. |
| 13   | User Wallet Signs and Completes the Transaction | Wallet Integrations | The user’s wallet is prompted to sign the transaction, completing the process. |

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
| 4    | Backend Prepares Optimized Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data with gas optimizations for the smart contract call. | Calculates the output amount of DAI with minimized gas costs. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates token swap | Sends the prepared transaction data to the smart contract. | Sends swap details to the smart contract handling the liquidity pool. |
| 6    | Smart Contract Executes Swap | Smart Contracts | Performs token swap | Uses the CPMM formula to execute the swap with optimized gas usage. | Adjusts the balances of ETH and DAI in the liquidity pool. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the swap details and outcome. | Emits events such as SwapExecuted with details of the tokens swapped and amounts. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed swap. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process. |

### Feature 8: Ethereum Integration

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Ethereum UI | Frontend Interface | Provides Ethereum network access | User connects to the Ethereum network through the interface. | User selects to connect their wallet to the Ethereum network. |
| 2    | Frontend Sends Connection Request | Frontend Interface → Backend Services | Initiates connection | User submits the connection request. | The frontend sends a request to the backend to connect to Ethereum nodes. |
| 3    | Backend Validates Connection | Backend Services | Ensures connection validity | Validates the connection request and establishes a link to Ethereum nodes. | Backend verifies the user's wallet and connects to Ethereum. |
| 4    | Backend Prepares Interaction Data | Backend Services | Formats data for Ethereum interaction | Prepares the necessary data for interacting with Ethereum smart contracts. | Backend prepares transaction data for the user's request. |
| 5    | Backend Calls the Ethereum Smart Contract | Backend Services → Smart Contracts | Initiates transaction | Sends the prepared transaction data to the Ethereum smart contract. | Sends transaction details to the smart contract on Ethereum. |
| 6    | Smart Contract Executes Transaction | Smart Contracts | Performs transaction | Executes the transaction on the Ethereum network. | The smart contract processes the transaction as per the request. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block on Ethereum. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the transaction details and outcome. | Emits events such as TransactionExecuted with details of the transaction. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed transaction. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the process. |

### Feature 9: ERC-20 to ERC-20 Swaps

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with ERC-20 Swap UI | Frontend Interface | Captures user input | User selects ERC-20 tokens to swap and enters the amount. | User selects to swap USDC for DAI and specifies the amount of USDC to swap. |
| 2    | Frontend Sends Swap Request | Frontend Interface → Backend Services | Communicates user's request | User submits the ERC-20 swap request. | The frontend sends a request containing the swap details to the backend service. |
| 3    | Backend Validates Request | Backend Services | Ensures request validity | Validates the swap request, checking for sufficient balance and valid token pairs. | Checks if the user has enough USDC in their wallet and if the USDC/DAI pair exists. |
| 4    | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the ERC-20 swap smart contract call. | Calculates the output amount of DAI based on the CPMM formula. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates token swap | Sends the prepared transaction data to the smart contract. | Sends swap details to the smart contract handling the liquidity pool. |
| 6    | Smart Contract Executes Swap | Smart Contracts | Performs token swap | Uses the CPMM formula to execute the ERC-20 to ERC-20 swap. | Adjusts the balances of USDC and DAI in the liquidity pool. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the swap details and outcome. | Emits events such as SwapExecuted with details of the tokens swapped and amounts. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed swap. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process. |

### Feature 10: Improved User Interface and Experience

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Enhanced UI | Frontend Interface | Provides enhanced user experience | User interacts with the improved UI for token swaps and liquidity provision. | User selects to swap ETH for DAI using the enhanced swap interface. |
| 2    | Frontend Sends Request to Backend | Frontend Interface → Backend Services | Communicates user's request | User submits the swap or liquidity provision request. | The frontend sends a request containing the details to the backend service. |
| 3    | Backend Validates and Processes Request | Backend Services | Ensures request validity | Validates and processes the user's request efficiently. | Backend checks if the user has enough tokens and prepares the transaction. |
| 4    | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the smart contract call. | Calculates the output amount of tokens based on the CPMM formula. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates transaction | Sends the prepared transaction data to the smart contract. | Sends transaction details to the smart contract handling the liquidity pool. |
| 6    | Smart Contract Executes Transaction | Smart Contracts | Performs transaction | Uses the CPMM formula to execute the swap or provision. | Adjusts the balances of tokens in the liquidity pool. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the transaction details and outcome. | Emits events such as TransactionExecuted with details of the transaction. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed transaction. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the process. |

Sure, here is the tabular representation of the flow of actions for each of the remaining features in UniSwap v4, starting from Feature 11:

### Feature 11: Support for ERC-20 Token Lists

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Token List UI | Frontend Interface | Provides token list UI | User navigates to the token list section to view supported ERC-20 tokens. | User selects to view the list of supported tokens. |
| 2    | Frontend Sends Request to Backend | Frontend Interface → Backend Services | Communicates user's request | User submits a request to view or update the token list. | The frontend sends a request to the backend to fetch the token list. |
| 3    | Backend Fetches Token List Data | Backend Services | Retrieves token list data | Fetches the list of supported ERC-20 tokens from the database or smart contract. | Backend retrieves the token list data from the storage. |
| 4    | Backend Prepares Token List Data | Backend Services | Formats data for frontend | Formats the token list data for display on the frontend interface. | Backend prepares the token list data in a user-friendly format. |
| 5    | Backend Sends Token List Data to Frontend | Backend Services → Frontend Interface | Provides token list data | Sends the formatted token list data to the frontend interface. | Backend sends the token list data to the frontend. |
| 6    | Frontend Updates Token List UI | Frontend Interface | Updates UI with token list | Displays the updated list of supported ERC-20 tokens. | Frontend shows the updated list of supported tokens. |
| 7    | User Selects Tokens for Swap | Frontend Interface | Captures user input | User selects ERC-20 tokens from the list for swapping. | User selects USDC and DAI from the token list for swapping. |
| 8    | Frontend Sends Swap Request | Frontend Interface → Backend Services | Communicates user's request | User submits the ERC-20 swap request. | The frontend sends a request containing the swap details to the backend service. |
| 9    | Backend Validates and Processes Request | Backend Services | Ensures request validity | Validates and processes the user's request efficiently. | Backend checks if the user has enough tokens and prepares the transaction. |
| 10   | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the smart contract call. | Calculates the output amount of tokens based on the CPMM formula. |
| 11   | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates transaction | Sends the prepared transaction data to the smart contract. | Sends transaction details to the smart contract handling the liquidity pool. |
| 12   | Smart Contract Executes Transaction | Smart Contracts | Performs transaction | Uses the CPMM formula to execute the swap. | Adjusts the balances of tokens in the liquidity pool. |
| 13   | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 14   | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the transaction details and outcome. | Emits events such as SwapExecuted with details of the tokens swapped and amounts. |
| 15   | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed swap. |
| 16   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process. |

### Feature 12: Concentrated Liquidity

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Liquidity Range UI | Frontend Interface | Captures user input | User selects tokens and specifies the range for providing liquidity. | User selects to provide liquidity for ETH/DAI within a specified price range. |
| 2    | Frontend Sends Liquidity Request | Frontend Interface → Backend Services | Communicates user's request | User submits the liquidity provision request. | The frontend sends a request containing the liquidity details to the backend service. |
| 3    | Backend Validates Request | Backend Services | Ensures request validity | Validates the liquidity request, checking for sufficient balance and valid range. | Checks if the user has enough tokens and if the specified range is valid. |
| 4    | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the liquidity provision smart contract call. | Calculates the share of liquidity based on the specified range. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates liquidity provision | Sends the prepared transaction data to the smart contract. | Sends liquidity details to the smart contract handling the liquidity pool. |
| 6    | Smart Contract Executes Provision | Smart Contracts | Performs liquidity provision | Adds the tokens to the pool and allocates liquidity within the specified range. | Adjusts the balances of tokens in the pool and issues liquidity tokens. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated pool balances are recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the provision details and outcome. | Emits events such as LiquidityAdded with details of the tokens provided and amounts. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed provision. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the provision process. |

### Feature 13: Multiple Fee Tiers

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Fee Tier UI | Frontend Interface | Captures user input | User selects tokens and specifies the fee tier for providing liquidity. | User selects to provide liquidity for ETH/DAI with a specific fee tier. |
| 2    | Frontend Sends Fee Tier Request | Frontend Interface → Backend Services | Communicates user's request | User submits the fee tier selection request. | The frontend sends a request containing the fee tier details to the backend service. |
| 3    | Backend Validates Request | Backend Services | Ensures request validity | Validates the fee tier request, checking for sufficient balance and valid fee tier. | Checks if the user has enough tokens and if the specified fee tier is valid. |
| 4    | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the liquidity provision smart contract call. | Calculates the share of liquidity based on the specified fee tier. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates liquidity provision | Sends the prepared transaction data to the smart contract. | Sends liquidity details to the smart contract handling the liquidity pool. |
| 6    | Smart Contract Executes Provision | Smart Contracts | Performs liquidity provision | Adds the tokens to the pool and allocates liquidity with the specified fee tier. | Adjusts the balances of tokens in the pool and issues liquidity tokens. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated pool balances are recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the provision details and outcome. | Emits events such as LiquidityAdded with details of the tokens provided and amounts. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed provision. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the provision process. |

### Feature 14: Non-Fungible Liquidity (NFT Positions)

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with NFT UI | Frontend Interface | Captures user input | User selects tokens and specifies the liquidity provision details to mint an NFT. | User selects to provide liquidity for ETH/DAI and specifies the amount. |
| 2    | Frontend Sends NFT Request | Frontend Interface → Backend Services | Communicates user's request | User submits the liquidity provision request. | The frontend sends a request containing the liquidity details to the backend service. |
| 3    | Backend Validates Request | Backend Services | Ensures request validity | Validates the liquidity request, checking for sufficient balance and valid parameters. | Checks if the user has enough tokens and if the specified parameters are valid. |
| 4    | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the liquidity provision smart contract call. | Calculates the share of liquidity based on the specified parameters. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates liquidity provision | Sends the prepared transaction data to the smart contract. | Sends liquidity details to the smart contract handling the liquidity pool. |
| 6    | Smart Contract Mints NFT | Smart Contracts | Mints NFT representing liquidity position | Adds the tokens to the pool and mints an NFT representing the user's liquidity position. | Adjusts the balances of tokens in the pool and issues an NFT to the user. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated pool balances and NFT issuance are recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the provision details and outcome. | Emits events such as LiquidityAdded with details of the tokens provided and NFT issued. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed provision and the issued NFT. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the provision process.

### Feature 15: Dynamic Fee Switching

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Fee Switching UI | Frontend Interface | Captures user input | User selects tokens and specifies the fee switching parameters. | User selects to switch the fee tier for their liquidity provision. |
| 2    | Frontend Sends Fee Switching Request | Frontend Interface → Backend Services | Communicates user's request | User submits the fee switching request. | The frontend sends a request containing the fee switching details to the backend service. |
| 3    | Backend Validates Request | Backend Services | Ensures request validity | Validates the fee switching request, checking for sufficient balance and valid parameters. | Checks if the user has enough tokens and if the specified parameters are valid. |
| 4    | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the fee switching smart contract call. | Calculates the new fee tier and prepares the data for the smart contract. |
| 5    | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates fee switching | Sends the prepared transaction data to the smart contract. | Sends fee switching details to the smart contract handling the liquidity pool. |
| 6    | Smart Contract Adjusts Fee | Smart Contracts | Adjusts fee according to new parameters | Updates the fee tier for the user's liquidity provision based on the new parameters. | Adjusts the fee structure in the liquidity pool according to the new fee tier. |
| 7    | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated fee tier is recorded. |
| 8    | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the fee switching details and outcome. | Emits events such as FeeSwitched with details of the new fee tier. |
| 9    | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed fee switching. |
| 10   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the fee switching process.

### Feature 16: Decentralized Price Oracles

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Price Data UI | Frontend Interface | Displays price data | User views real-time price data for tokens. | User checks the current price of ETH in DAI on the interface. |
| 2    | Frontend Sends Price Data Request | Frontend Interface → Backend Services | Communicates user's request | User requests real-time price data. | The frontend sends a request to the backend to fetch current price data. |
| 3    | Backend Fetches Price Data from Oracles | Backend Services | Retrieves price data | Fetches real-time price data from decentralized oracles. | Backend retrieves the price of ETH from multiple oracles. |
| 4    | Backend Aggregates Price Data | Backend Services | Aggregates and formats data | Aggregates price data from multiple sources and formats it for display. | Backend calculates the average price of ETH based on data from different oracles. |
| 5    | Backend Sends Aggregated Data to Frontend | Backend Services → Frontend Interface | Provides aggregated price data | Sends the aggregated price data to the frontend interface. | Backend sends the average price of ETH to the frontend. |
| 6    | Frontend Updates Price Data UI | Frontend Interface | Updates UI with price data | Displays the updated real-time price data. | Frontend shows the current average price of ETH in the swap interface. |
| 7    | User Initiates Transaction Based on Price Data | Frontend Interface | Captures user input | User initiates a token swap based on the displayed price data. | User decides to swap ETH for DAI based on the current price. |
| 8    | Frontend Sends Swap Request | Frontend Interface → Backend Services | Communicates user's request | User submits the token swap request. | The frontend sends a request containing the swap details to the backend service. |
| 9    | Backend Validates and Processes Request | Backend Services | Ensures request validity | Validates and processes the user's request efficiently. | Backend checks if the user has enough tokens and prepares the transaction. |
| 10   | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the smart contract call. | Calculates the output amount of tokens based on the CPMM formula. |
| 11   | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates transaction | Sends the prepared transaction data to the smart contract. | Sends transaction details to the smart contract handling the liquidity pool. |
| 12   | Smart Contract Executes Transaction | Smart Contracts | Performs transaction | Uses the CPMM formula to execute the swap. | Adjusts the balances of tokens in the liquidity pool. |
| 13   | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 14   | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the transaction details and outcome. | Emits events such as SwapExecuted with details of the tokens swapped and amounts. |
| 15   | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed swap. |
| 16   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process.

### Feature 17: Improved Price Oracles

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Enhanced Price Data UI | Frontend Interface | Displays enhanced price data | User views real-time price data for tokens with improved accuracy. | User checks the current price of ETH in DAI on the interface. |
| 2    | Frontend Sends Price Data Request | Frontend Interface → Backend Services | Communicates user's request | User requests real-time price data. | The frontend sends a request to the backend to fetch current price data. |
| 3    | Backend Fetches Price Data from Oracles | Backend Services | Retrieves price data | Fetches real-time price data from improved decentralized oracles. | Backend retrieves the price of ETH from multiple improved oracles. |
| 4    | Backend Aggregates Price Data | Backend Services | Aggregates and formats data | Aggregates price data from multiple sources and formats it for display. | Backend calculates the average price of ETH based on data from different oracles. |
| 5    | Backend Sends Aggregated Data to Frontend | Backend Services → Frontend Interface | Provides aggregated price data | Sends the aggregated price data to the frontend interface. | Backend sends the average price of ETH to the frontend. |
| 6    | Frontend Updates Price Data UI | Frontend Interface | Updates UI with price data | Displays the updated real-time price data. | Frontend shows the current average price of ETH in the swap interface. |
| 7    | User Initiates Transaction Based on Price Data | Frontend Interface | Captures user input | User initiates a token swap based on the displayed price data. | User decides to swap ETH for DAI based on the current price. |
| 8    | Frontend Sends Swap Request | Frontend Interface → Backend Services | Communicates user's request | User submits the token swap request. | The frontend sends a request containing the swap details to the backend service. |
| 9    | Backend Validates and Processes Request | Backend Services | Ensures request validity | Validates and processes the user's request efficiently. | Backend checks if the user has enough tokens and prepares the transaction. |
| 10   | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the smart contract call. | Calculates the output amount of tokens based on the CPMM formula. |
| 11   | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates transaction | Sends the prepared transaction data to the smart contract. | Sends transaction details to the smart contract handling the liquidity pool. |
| 12   | Smart Contract Executes Transaction | Smart Contracts | Performs transaction | Uses the CPMM formula to execute the swap. | Adjusts the balances of tokens in the liquidity pool. |
| 13   | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 14   | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the transaction details and outcome. | Emits events such as SwapExecuted with details of the tokens swapped and amounts. |
| 15   | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed swap. |
| 16   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process.

### Feature 18: Oracle Integration

| Step | Action | Component | Role | Description | Example |
|------|--------|-----------|------|-------------|---------|
| 1    | User Interaction with Oracle Data UI | Frontend Interface | Displays oracle data | User views real-time data provided by oracles. | User checks the current price of ETH in DAI on the interface. |
| 2    | Frontend Sends Oracle Data Request | Frontend Interface → Backend Services | Communicates user's request | User requests real-time data from oracles. | The frontend sends a request to the backend to fetch data from oracles. |
| 3    | Backend Fetches Data from Oracles | Backend Services | Retrieves oracle data | Fetches real-time data from integrated oracles. | Backend retrieves the price of ETH from multiple oracles. |
| 4    | Backend Aggregates Oracle Data | Backend Services | Aggregates and formats data | Aggregates data from multiple oracles and formats it for display. | Backend calculates the average price of ETH based on data from different oracles. |
| 5    | Backend Sends Aggregated Data to Frontend | Backend Services → Frontend Interface | Provides aggregated oracle data | Sends the aggregated data to the frontend interface. | Backend sends the average price of ETH to the frontend. |
| 6    | Frontend Updates Oracle Data UI | Frontend Interface | Updates UI with oracle data | Displays the updated real-time data from oracles. | Frontend shows the current average price of ETH in the swap interface. |
| 7    | User Initiates Transaction Based on Oracle Data | Frontend Interface | Captures user input | User initiates a token swap based on the displayed oracle data. | User decides to swap ETH for DAI based on the current price. |
| 8    | Frontend Sends Swap Request | Frontend Interface → Backend Services | Communicates user's request | User submits the token swap request. | The frontend sends a request containing the swap details to the backend service. |
| 9    | Backend Validates and Processes Request | Backend Services | Ensures request validity | Validates and processes the user's request efficiently. | Backend checks if the user has enough tokens and prepares the transaction. |
| 10   | Backend Prepares Transaction Data | Backend Services | Formats data for smart contract | Prepares the transaction data for the smart contract call. | Calculates the output amount of tokens based on the CPMM formula. |
| 11   | Backend Calls the Smart Contract | Backend Services → Smart Contracts | Initiates transaction | Sends the prepared transaction data to the smart contract. | Sends transaction details to the smart contract handling the liquidity pool. |
| 12   | Smart Contract Executes Transaction | Smart Contracts | Performs transaction | Uses the CPMM formula to execute the swap. | Adjusts the balances of tokens in the liquidity pool. |
| 13   | Blockchain Confirms the Transaction | Blockchain Network | Ensures transaction validity | Validates and confirms the transaction. | The transaction is included in a new block and updated token balances are recorded. |
| 14   | Smart Contract Emits Events | Smart Contracts → Backend Services | Provides transaction details | Emits events indicating the transaction details and outcome. | Emits events such as SwapExecuted with details of the tokens swapped and amounts. |
| 15   | Backend Updates User Interface | Backend Services → Frontend Interface | Provides feedback to user | Retrieves transaction status and updates the frontend interface. | Displays a confirmation message with details of the completed swap. |
| 16   | User Wallet Signs and Completes Transaction | Wallet Integrations | Authorizes transaction | Prompts the user's wallet to sign the transaction. | The user signs the transaction using their wallet, completing the swap process.

