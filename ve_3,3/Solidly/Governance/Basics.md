### Basics

#### The Key to SOLID Emissions

**Liquidity Acquisition**
- **Purpose**: Attract users and liquidity.
- **Incentives**: Directed towards pools generating the highest fees for voters.
- **Self-Optimization**: Voters pursue the best APRs, aligning their interests with the protocol’s success.

#### Voting NFT (veSOLID)
- **Mechanism**: Users lock SOLID into veSOLID (vote-escrowed).
- **Transferability**: Unlike Curve, veSOLID positions are tokenized as NFTs (ERC-721), making them tradable and addressing capital inefficiency.

#### Voting Power
- **Calculation**: Total SOLID locked into veSOLID NFTs multiplied by the linear time decay.
- **Example**: 1 SOLID locked for 4 years = voting weight of 1. 
- **Total Voting Power**: If 60,000,000 SOLID are locked for 3 years, the voting weight = 45,000,000.

#### Rewards Distribution
- **Mechanism**: Aggregates all rewards through RewardDistributor.sol.
- **Process**: Off-chain accounting pushed to the contract as a merkle root.
- **Claiming**: Users provide merkle proof to claim rewards.
- **Security**: PauseClaims function allows users to stop claims if errors are detected.
- **Transparency**: All data used for calculations is published for verification.
