# Pool Share Calculation Function

The number of shares in each pool is determined using this all-important constant function:

LiquidityShares_{numberOfOutcomes} = SharesOutcomeA + SharesOutcomeB + SharesOutcomeC + SharesOutcomeD + ...

So, for example, in a market with two outcomes, the function would be:

LiquidityShares^2 = SharesOutcomeA + SharesOutcomeB

Whereas in a market with five outcomes, we'd get:

LiquidityShares^5 = SharesOutcomeA + SharesOutcomeB + SharesOutcomeC + SharesOutcomeD + SharesOutcomeE

Example 1: Two Outcomes  

In a market with two outcomes, let's assume the shares are as follows:

- SharesOutcomeA: 150 
- SharesOutcomeB: 100

 The function would be: 
[ LiquidityShares^2 = 150 + 100 = 250 ]

Example 2: Five Outcomes  
In a market with five outcomes, let's assume the shares are as follows:
- SharesOutcomeA: 120
- SharesOutcomeB: 80
- SharesOutcomeC: 50
- SharesOutcomeD: 30
- SharesOutcomeE: 20

The function would be:
[LiquidityShares}^5 = 120 + 80 + 50 + 30 + 20 = 300 ]



# Outcome Price Calculation Function

## Price calculation in a binary outcome market

In a binary outcome market (a market with only two outcomes), the formula used to determine outcome prices is the following:

PriceOutcomeA = SharesOutcomeB / sum(AllOutcomeShares)

PriceOutcomeB = SharesOutcomeA / sum(AllOutcomeShares)

Example 1

 SharesOutcomeA: 150
 SharesOutcomeB: 100

The prices would be:

[ PriceOutcomeA = frac{100}{150 + 100} = frac{100}{250} = 0.4 ]

[ PriceOutcomeB = frac{150}{150 + 100} = frac{150}{250} = 0.6 ]


## Price calculation in a multiple outcome market

In a market with multiple outcomes, the formula becomes a bit more complex. Before we can calculate the outcome prices, we must first calculate their relative weight.

To be clear, this same formula works for outcome price calculation in a binary outcome market as well, but is not necessary.

To calculate the Price Weight for a given outcome, we multiply the number of shares available in the pool of every other outcome.

OutcomePriceWeight = Product(SharesOfAllOtherOutcomes)

Once we have the Price Weight of every Outcome, we can determine the price on an outcome.
OutcomePrice = OutcomePriceWeight / sum(PriceWeightOfAllOutcomes)

Example 

**Example 2: Multiple Outcome Market**  

Let's assume the shares are as follows:

 SharesOutcomeA: 120
 
 SharesOutcomeB: 80
 
 SharesOutcomeC: 50
 
 SharesOutcomeD: 30
 
SharesOutcomeE: 20

Calculating the Price Weight for OutcomeA:

[PriceWeightA = {SharesOutcomeB} * {SharesOutcomeC} * {SharesOutcomeD} * {SharesOutcomeE} = 80 * 50 * 30 * 20 = 2,400,000 ]

Calculating the Price Weight for OutcomeB:

[ {PriceWeightB} = {SharesOutcomeA} * {SharesOutcomeC} * {SharesOutcomeD} * {SharesOutcomeE} = 120 * 50 * 30 * 20 = 3,600,000 ]

Calculating the Price Weight for OutcomeC:

[ PriceWeightC} = {SharesOutcomeA} * {SharesOutcomeB} * {SharesOutcomeD} * {SharesOutcomeE} = 120 *  80 * 30 * 20 = 5,760,000 ]

Calculating the Price Weight for OutcomeD:

[ {PriceWeightD} = {SharesOutcomeA} * {SharesOutcomeB} * {SharesOutcomeC} * {SharesOutcomeE} = 120 *  80 * 50 * 20 = 9,600,000 ]

Calculating the Price Weight for OutcomeE:

[ {PriceWeightE = {SharesOutcomeA} * {SharesOutcomeB} * {SharesOutcomeC} * {SharesOutcomeD} = 120 * 80 * 50 * 30 = 14,400,000 ]

Total Price Weight:

[ {TotalPriceWeight} = {PriceWeightA} + {PriceWeightB} + {PriceWeightC} + {PriceWeightD} + {PriceWeightE} = 2,400,000 + 3,600,000 + 5,760,000 + 9,600,000 + 14,400,000 = 35,760,000 ]

The prices for each outcome would be:

[ {OutcomePriceA} = {PriceWeightA}/{TotalPriceWeight}} = {2,400,000}/{35,760,000} = 0.067 ]

[ {OutcomePriceB} = {PriceWeightB}/{TotalPriceWeight} = {3,600,000}/{35,760,000} = 0.101 ]

[ {OutcomePriceC} = {PriceWeightC}/{TotalPriceWeight} = {5,760,000}/{35,760,000} = 0.161 ]

[ {OutcomePriceD} = {PriceWeightD}/{TotalPriceWeight} = {9,600,000}/{35,760,000} = 0.268 ]

[ {OutcomePriceE} = {{PriceWeightE}{{TotalPriceWeight} ={14,400,000}/{35,760,000} = 0.403 ]

