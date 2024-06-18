

| **Contract Name**      | **Primary Functionalities**                                                                                                                     |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **PoolFactory**        | - Responsible for creating and managing liquidity pools.<br>- Allows configuration of pools, including pausing and setting custom fees.<br>- Handles pool upgradability and ensures proper initialization of new pools. |
| **Router**             | - Supports complex operations like multi-pool swaps and LP deposits/withdrawals.<br>- Enables zapping in/out of pools from any ERC20 token.<br>- Handles transactions involving fee-on-transfer tokens. |
| **FactoryRegistry**    | - Maintains a registry of all factory contracts (pool, gauge, bribe, and rewards).<br>- Ensures all swaps and interactions are validated against registered factories.<br>- Used in governance to approve or reject new factories. |
| **RewardsDistributor** | - Calculates and distributes rebases based on the VELO locked and unlocked just before each epoch transition.<br>- Handles claims of rewards by NFT owners, distributing based on contribution to locked VELO. |
| **Gauge**              | - Distributes protocol emissions to liquidity providers proportionate to their pool share.<br>- Allows LPs to deposit and withdraw tokens.<br>- Manages additional emissions and fee redirection for enhanced rewards. |
| **Voter**              | - Manages all voting related functions, including casting votes and handling emissions distribution to gauges.<br>- Supports specialized operations for managed NFTs, such as deposits and withdrawals.<br>- Ensures liveness of gauges and proper reward distribution during epoch transitions. |
| **VotingReward**       | - Distributes voting rewards, which include fees and bribes, to NFT owners based on their votes for specific pools.<br>- Manages fee and bribe accrual and distribution cycle. |
| **ManagedReward**      | - Manages rewards for managed NFTs, ensuring distribution is in line with deposits and the management protocol.<br>- Handles the complexities of rewards accruement and distribution for managed NFTs. |



