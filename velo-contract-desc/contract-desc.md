

| **Contract Name**      | **Primary Functionalities**                                                                                                                     |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pool**        | - Implements a token pool for Velodrome V2, supporting both stable and volatile pools. <br> - Handles token swapping, minting, burning, fee collection, and liquidity management. <br> - Calculates output amounts for token swaps, manages reserves, and updates price accumulators. <br> - Integrates with IPoolCallee for callback functions, enabling flash loan functionality. <br> - Utilizes OpenZeppelin libraries for security and mathematical operations.|  
| **PoolFees**        | - Manages fee collection and distribution for the Pool contract. <br> - Allows the pool to transfer accumulated fees to users. <br> - Ensures fee handling is segregated from core liquidity operations, enhancing security. |
| **Router**             | - Supports complex operations like multi-pool swaps and LP deposits/withdrawals.<br>- Enables zapping in/out of pools from any ERC20 token.<br>- Handles transactions involving fee-on-transfer tokens. |
| **RewardsDistributor** | - Calculates and distributes rebases based on the VELO locked and unlocked just before each epoch transition.<br>- Handles claims of rewards by NFT owners, distributing based on contribution to locked VELO. |
| **VeArtProxy** | - Generates dynamic SVG artwork for veNFTs based on token-specific attributes. <br> - Uses pseudorandom seed generation for creating unique line art shapes. <br> - Supports various geometric shapes and line art styles, enhancing visual uniqueness. <br> - Encodes metadata and artwork in Base64 format for compatibility with NFT standards. <br> - Interfaces with the Voting Escrow contract to fetch token attributes and balances. |
| **Velo** | - Defines the native token for the Velodrome V2 ecosystem, named VELO. <br> - Inherits from ERC20 and ERC20Permit to provide standard token functionalities and permit-based approvals. <br> - Manages the minting of tokens, restricted to the designated minter. <br> - Allows setting a new minter through the setMinter function, restricted to the current minter. |





