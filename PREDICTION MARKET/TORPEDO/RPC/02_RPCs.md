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

##### Events
- **EventsController.ts**
  - **Task:** Handles HTTP requests and responses for event-related operations.
- **EventsDTO.ts**
  - **Task:** Defines the Data Transfer Object for event operations.
- **EventsSchema.ts**
  - **Task:** Defines the validation schema for event-related data.
- **EventsUseCase.ts**
  - **Task:** Contains the core business logic for event operations.
- **index.ts**
  - **Task:** Aggregates and exports the use case components for easy import elsewhere in the application.

#### `src/workers`
- **BaseWorker.ts**
  - **Task:** Defines a base class for workers, providing common functionality and structure that other workers can extend.
- **EventsWorker.ts**
  - **Task:** Implements a worker specifically for handling event-related background tasks, using the structure provided by BaseWorker.

#### `src/app.ts`
- **Task:** The main application setup file where the Express app is configured. This includes middleware setup, route definitions, and other app-wide configurations.

#### `src/index.ts`
- **Task:** The entry point of the application. It typically starts the server, connects to databases, and performs any necessary initialization.

#### `src/queues.ts`
- **Task:** Sets up and manages BullMQ queues, defining how different types of jobs are processed and how the queues are monitored.

#### `src/routes.ts`
- **Task:** Defines the routes for the Express application, mapping endpoints to their respective controllers and middleware.

In a tabular form:

| Directory/File                        | Task Description |
|---------------------------------------|------------------|
| `src`                                 | Main source directory containing all the code for the application. |
| `src/middlewares`                     | Contains middleware functions. |
| `Yup.ts`                              | Middleware for schema validation using Yup. |
| `src/models`                          | Defines data models. |
| `contract.ts`                         | Defines the data model for contracts. |
| `index.ts`                            | Aggregates and exports models in the directory. |
| `src/providers`                       | Contains providers and their implementations. |
| `ContractProviders.ts`                | Defines the interface for contract providers. |
| `implementations`                     | Contains implementations of providers. |
| `PolkamarketsContractsProviders.ts`   | Implements contract provider for Polkamarkets. |
| `src/services`                        | Provides various services. |
| `Etherscan.ts`                        | Provides services for interacting with Etherscan API. |
| `RedisServices.ts`                    | Provides services for interacting with Redis. |
| `src/usecases`                        | Contains the use case logic of the application. |
| `Call`                                | Handles call-related operations. |
| `CallController.ts`                   | Handles HTTP requests and responses for call operations. |
| `CallDTO.ts`                          | Defines the Data Transfer Object for call operations. |
| `CallSchema.ts`                       | Defines the validation schema for call data. |
| `CallUseCase.ts`                      | Contains the core business logic for call operations. |
| `index.ts` (in Call)                  | Aggregates and exports call use case components. |
| `Events`                              | Handles event-related operations. |
| `EventsController.ts`                 | Handles HTTP requests and responses for event operations. |
| `EventsDTO.ts`                        | Defines the Data Transfer Object for event operations. |
| `EventsSchema.ts`                     | Defines the validation schema for event data. |
| `EventsUseCase.ts`                    | Contains the core business logic for event operations. |
| `index.ts` (in Events)                | Aggregates and exports event use case components. |
| `src/workers`                         | Manages background tasks. |
| `BaseWorker.ts`                       | Defines a base class for workers. |
| `EventsWorker.ts`                     | Worker for handling event-related background tasks. |
| `src/app.ts`                          | Main application setup file for configuring the Express app. |
| `src/index.ts`                        | Entry point of the application, starts the server and initializes connections. |
| `src/queues.ts`                       | Sets up and manages BullMQ queues. |
| `src/routes.ts`                       | Defines the routes for the Express application. |
