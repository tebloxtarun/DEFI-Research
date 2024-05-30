### Directory and File Structure

#### `src`
- **Purpose:** The main source directory containing all the code for the application.

#### `src/middlewares`
- **Yup.ts**
  - **Task:** Contains middleware functions for schema validation using Yup. This is typically used to validate incoming requests to ensure they meet the expected schema before processing.

#### `src/models`
- **contract.ts**
  - **Task:** Defines the data model for contracts, including properties and possibly methods related to contract entities.
- **index.ts**
  - **Task:** Aggregates and exports the models in the directory for easy import elsewhere in the application.

#### `src/providers`
- **ContractProviders.ts**
  - **Task:** Defines the interface or abstract class for contract providers, specifying methods that any contract provider implementation must follow.
- **implementations**
  - **PolkamarketsContractsProviders.ts**
    - **Task:** Implements the contract provider interface specifically for Polkamarkets, detailing how to interact with Polkamarkets contracts.

#### `src/services`
- **Etherscan.ts**
  - **Task:** Provides services related to interacting with the Etherscan API, such as fetching transaction details or contract information.
- **RedisServices.ts**
  - **Task:** Provides services for interacting with a Redis instance, such as caching data, managing sessions, or storing temporary data.

#### `src/usecases`
- **Purpose:** Contains the use case logic of the application, segregated into different functional areas.

##### Call
- **CallController.ts**
  - **Task:** Handles HTTP requests and responses for call-related operations, coordinating between the client and the use case logic.
- **CallDTO.ts**
  - **Task:** Defines the Data Transfer Object for call operations, ensuring consistent data structure between different layers of the application.
- **CallSchema.ts**
  - **Task:** Defines the validation schema for call-related data using a validation library like Yup.
- **CallUseCase.ts**
  - **Task:** Contains the core business logic for call operations, implementing the main functionality required for handling calls.
- **index.ts**
  - **Task:** Aggregates and exports the use case components for easy import elsewhere in the application.

