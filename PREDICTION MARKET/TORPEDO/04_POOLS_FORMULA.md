# Pool Share Calculation Function

The number of shares in each pool is determined using this all-important constant function:

LiquidityShares_{numberOfOutcomes} = SharesOutcomeA + SharesOutcomeB + SharesOutcomeC + SharesOutcomeD + ...

So, for example, in a market with two outcomes, the function would be:

LiquidityShares^2 = SharesOutcomeA + SharesOutcomeB

Whereas in a market with five outcomes, we'd get:

LiquidityShares^5 = SharesOutcomeA + SharesOutcomeB + SharesOutcomeC + SharesOutcomeD + SharesOutcomeE

# Outcome Price Calculation Function

## Price calculation in a binary outcome market

In a binary outcome market (a market with only two outcomes), the formula used to determine outcome prices is the following:

PriceOutcomeA = SharesOutcomeB / sum(AllOutcomeShares)

PriceOutcomeB = SharesOutcomeA / sum(AllOutcomeShares)

## Price calculation in a multiple outcome market

In a market with multiple outcomes, the formula becomes a bit more complex. Before we can calculate the outcome prices, we must first calculate their relative weight.

To be clear, this same formula works for outcome price calculation in a binary outcome market as well, but is not necessary.

To calculate the Price Weight for a given outcome, we multiply the number of shares available in the pool of every other outcome.

OutcomePriceWeight = Product(SharesOfAllOtherOutcomes)

Once we have the Price Weight of every Outcome, we can determine the price on an outcome.
OutcomePrice = OutcomePriceWeight / sum(PriceWeightOfAllOutcomes)
