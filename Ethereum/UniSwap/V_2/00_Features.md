Key Features of Uniswap v2

1. Arbitrary Pairs Between ERC-20 Tokens:
In Uniswap v1, pairs could only be created with ETH as one of the tokens. Uniswap v2 removes this restriction, allowing direct pairs between any two ERC-20 tokens. This increases the flexibility and utility of the protocol.
Hardened Price Oracle:

2. Uniswap v2 includes a robust price oracle mechanism that enables other smart contracts to obtain a time-weighted average price (TWAP) over a specified interval. This feature improves the reliability of price feeds and reduces the susceptibility to short-term price manipulation.
Flash Swaps:

3. Flash swaps in Uniswap v2 allow users to receive tokens from a pool and use them elsewhere within the same transaction before returning them. If the tokens are not returned by the end of the transaction, an equivalent value in the other token of the pair must be paid. This feature facilitates arbitrage and other complex trading strategies.
Protocol Fee:

4. Uniswap v2 introduces a mechanism for an optional protocol fee that can be activated in the future. This fee would divert a small portion of the trading fees to support the ongoing development and maintenance of the protocol. By default, this fee is set to zero but can be turned on through governance.
Re-architected Contracts:

5. The core contracts in Uniswap v2 have been redesigned to minimize the attack surface, improving the overall security and robustness of the protocol. This includes modular and clean contract structures that facilitate better auditing and understanding.
