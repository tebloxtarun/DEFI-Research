# SWAP.SOL #
https://github.com/balancer/balancer-v2-monorepo/blob/master/pkg/vault/contracts/Swaps.sol

Certainly! Here's a comprehensive breakdown of all the public and private functions in the provided `Swaps` contract:
### Public Functions:
1. `swap`: Allows users to perform a single token swap with a Balancer pool.
2. `batchSwap`: Allows users to perform multiple token swaps in a batch with Balancer pools.
3. `queryBatchSwap`: Allows users to simulate multiple token swaps in a batch and retrieve the resulting token deltas without affecting on-chain state.

### External Functions (View and Pure):
None of the functions in the provided contract are marked as external. However, the `queryBatchSwap` function, while not marked as external, can be called externally to simulate swaps.

### Internal Functions (Private):
1. `_swapWithPools`: Performs multiple swaps with Balancer pools internally.
2. `_swapWithPool`: Performs a single swap with a Balancer pool internally.
3. `_tokenGiven`: Helper function to determine the "given" token in a swap.
4. `_tokenCalculated`: Helper function to determine the "calculated" token in a swap.
5. `_getAmounts`: Helper function to calculate the amount in and amount out for a swap.
6. `_callMinimalSwapInfoPoolOnSwapHook`: Calls the `onSwap` hook for a pool that implements `IMinimalSwapInfoPool`.
7. `_processTwoTokenPoolSwapRequest`: Processes a swap request for a two-token pool.
8. `_processMinimalSwapInfoPoolSwapRequest`: Processes a swap request for a minimal swap info pool.
9. `_processGeneralPoolSwapRequest`: Processes a swap request for a general pool.
10. `_handleRemainingEth`: Handles any remaining ETH after swaps.
11. Helper functions used internally for swap logic, balance handling, and error checking.

All public and private functions in the contract are accounted for in this breakdown, ensuring that no function is left out.
