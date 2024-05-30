
## Market Resolution 
### THE MARKET TOKEN HAS BEEN NAMED AS **POLK**

Prediction Markets require that someone decides the correct outcome of an event, so that the market can be resolved. This is the point when the correct outcome, i.e., what truly happened in the real world, is reflected in the market. The people that resolve markets are called Oracles, and deciding the correct outcome is called “resolving a market”.

Whether it is economic indicators, outcomes of political or societal events, weather data, traffic status, stock and crypto prices, or even sports results, real-world data is needed to resolve a market.

In TORPEDO Prediction Markets, a “resolution source URL” and a Description are required when creating a market, so that all participants know what the criteria and source-of-truth for resolving the market are.

For example, consider the market “Will monkeypox be named a pandemic by the WHO by the end of January 2023?”. The resolution source for this market will likely be official WHO data. How can that data be passed on the market, so that it can be resolved?

Smart contracts are only aware of what happens on-chain, and oftentimes need inputs of reliable external data. Ideally, real-time and automated data, but obtaining correct data this way is not always possible. Above all, market resolution needs to be indisputable.

So, where does the off-chain information used to correctly resolve markets come from? It can come from a centralized third party, such as an automated data feed run in an Oracle Protocol like Chainlink. Or it can come from individuals, the crowd, whose wisdom can be tapped into and incentivized using web3 mechanisms.

The Torpedo Protocol currently uses a distributed consensus model, tapping into the wisdom of the crowd and rewarding those who participate, to determine the correct outcome of each prediction market once they expire. 

This process has worked fantastically so far. Out of the 2670 markets created across all chains and versions of TORPEDO, only twice has the Optimistic Oracle resolved a market incorrectly, amounting to a 99.9% success rate. In both cases, markets were small, and the participants ignored how the resolution process was managed, resulting in a wrongful resolution.

Despite the system's success, there is a theoretical problem with its design. While the system makes it exponentially more risky to try to cheat the result of the market – a malicious actor stands to lose an exponentially larger amount of bonded POLK with every wrongful bond – it still gives an advantage to users who hold large amounts of POLK. Even though no “bonding war” was ever observed on Torpedo, the potential problem exists.

For that reason, TORPEDO also supports a fail-safe mechanism that allows any user to bypass the Optimistic Oracle by summoning a Kleros Court so that a jury will impartially decide what the correct outcome of a market is.

#### How does Market Resolution work on TORPEDO ?

**The Optimistic Oracle Process:**
- Once a market’s expiration date has elapsed, any participant can place a POLK bond of any amount on the outcome that they believe is correct.
- Bonds can be challenged by other participants to ensure that nobody cheats. To challenge a bond, any participant can post a higher bond on a different outcome. The amount of POLK of the challenging bond needs to be twice the amount previously bonded.
- Every time a bond is placed, a 3-day lockup period starts. When the lockup period lapses, the final unchallenged bond wins, and the chosen outcome is accepted as correct and final.
- The participant who placed the final bond can claim their entire bond amount back, plus any amount bonded to incorrect outcomes, minus any amount previously bonded to the correct outcome.
- Any participant who bonded the correct outcome can claim back the amount they bonded on that outcome.
- Participants who bonded the wrong outcomes will lose the right to claim back the amount they bonded.

🚨 Note that it only makes sense to place a higher bond on a different outcome than the one that is currently bonded (i.e., to challenge it). Placing a higher bond on the currently bonded outcome will not yield any rewards.


