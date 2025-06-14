Economics attribution
Move to some common time point

July23 Portfolio, July23 RFR
July23 Portfolio, Dec23 RFR

July24 Portfolio, Dec23 RFR
July24 Portfolio, July24 RFR

A + B = Econimic impact from July23 to July24

Not entirely accurate because portfolio differences may cause different sensitivity to RFR

Charge to insurance fund > Not immediate impact to NBEV, but may cause impact when got overrun and need to increase expense assumption (Not immediate impact)

Some companies charge SE overrun to VNB to account for it

SSP is a drug
Easy sales but low margin
Group is strict
Profit driven, get profit no matter what, no sales in their KPI

Prophet Level
Specifies the order of calculations
Lower level goes first

Usually set like
Product > Accumulation > Summary

NB model point file include lapsed policies

Already accounted for via lapse assumption

Adjusted Net Worth = Net Assets, what the company owns
Par fund owned by policyholder so no ANW

Prophet Sequence
Convert MPF into Binary Format -> Read Binary Format to run

Index can select multiple rows and columns, 2D filter

BP projection methodology
Cross multiplication
But assumes the same portfolio mix for all

Performance management - all about the final result, are we on track to hit it

Management cares a lot more when behind

People scrutinise more when bad

Write down NBEV
Charges to shf
Not accounted for in assumption

Bad times ppl will scrutinise more

Actual Variance won’t his NBEV, but may cause assumption change
Actual variance will hit EV via ANW
Future effect is both Reserves and PVFP
Hard to get the pure FUTURE expected impact due to death/lapse in the first year because they are connected
Use stepwise method with 100% shock to isolate the effects

From a Profit Projection perspective
Remember that the reserve basis and the NBEV basis is completely different
The reserve pattern influences the profit pattern
Everything in NBEV is affected by RDR only, not Risk Free Rate
Mathematically, your reserve is the discount of the net cashflow in each period
If your net outflow is always positive, then you will always have reserve

Definition of operating are things within Management Control but what management define that have control in can be quite different

RFR
Unit price movement

Generally seen as Non Operating
Lock in at previous year end rates
BEIE > Cannot control investment performance but can control SAA, operating or not?
See what you want to recognise

Allocation do good, good if can recognise if not also wasted, but downside risk as well



If the portfolio mix is good or bad, can distort the results greatly


Key difference between insurance and other retail

Retail only has so many permutations

Insurance has many permutations, harder to track mix

Sense check is mostly about proportionality

Move 1%, should it move more or less by 1%

Direction

Magnitude

Key idea is to reduce the problem to a very simple scenario
 0 difference is the worse - Means offsetting

Loading is the same for each channel

Because unfair to the channels
Why their channel have more money to sell etc, tough conversation

Sense check
Direction
Magnitude - Proportionality to change, materiality

Reporting - consistency is very important
AoM -> Variance must be consistent with Experience Study
AoM -> ANW variance must be consistent with RBC2

Fair value is the market value
Fair value gain or loss is the change in market value

IOR = Operating Profit = Revenue - Expenses - Change in Fair value

Change in MV is excluded because that is outside of the control of management
Income = Premiums (FY + Renewal) - Reinsurance + ILP Fee Income + Investment Income + (Change in fair value)
Expenses = Benefit Outgo + change in reserves + expenses (INterestm Selling Expenses, Management Expenses)

Net Surplus (Profit) = Revenue - Expenses
Underwriting Profit = Revenue - Expenses - Investment Income - Chnage in fair value
** Operating Profit and Underwriting profit ar ejust different views of profit >> Underwriting only considers income/expenses from insurance business, operating considers things that are within the insurers scope


Management Reporting
Lock in assumptions because there are some assumptions that are out of management control > KPI should be set based on assumptions that they can control
EG. Capital > Can be managed, but also influenced by economic movement
EG. Diff companies diff practices

Monthly Monitoring
Risk of KPI reporting is that the final KPI is very different from expected
Monthly monitoring to reduce the risk of surprises

# **Business Planning**

Management Reporting is about communicating the **performance of the company** to management so that they can decide the strategic direction of the company moving forward. This process is internally known as **Business Planning**.

The financial performance of the company is measured through three metrics, known as **Key Peformance Index** (KPI):

* New Business Embedded Value (NBEV)
* Insurance Operating Results (IOR)
* Annual Premium Equivalent (APE)
* Each of the above components have different weightage to the overall financial performance

Business Planning comes in a few phases:

* **Baseline**: Setting target KPIs for the next three years (~August)
* **Rebase**: Adjusting target for the coming year based on the past year's performance (Start of the year)
* **Reforecast**: Gauge of whether the KPI for the current year will be hit (Middle of the year, may be more than once)

There are three levels to the KPI:

* **Threshold**: Lower bound; below this no bonus is paid
* **Budget**: Expected amount; beyond this amount the full bonus is paid
* **Stretch**: Upper bound of the KPI; beyond this additional bonus (1.3 times) is paid

The **forecasted** values for each of these metrics is known as the **Budget** amount. During the reforecast process, the **Actual** amount will be compared against the **Budget** to determine how "on track" the company is from the budget.

Through this process, management can determine how well each area is performing in the company. They can then take appropriate action to help bolster areas of the company that are under-performing.

## **Key Performance Index**

### **New Business Embedded Value**

**Embedded Value** (EV) is a measure of the profitability of a life insurance contract. It is typically measured for ALL in force contracts at the time of calculation. However, **New Business EV** (NBEV) thus represents the profitability of ONLY newly written business **within the year**.

> More details on the computation be found in a seperate note on EV.

NBEV is calculated as an **absolute value**, known as the **NBEV Dollar Amount**. However, absolute amounts are not very useful when measuring profitability. $10 profit given $100 revenue is much better than $10 profit given $1000 revenue. Thus, it is much better to consider the **Profit Margin** instead. In this context, it is referred to as the **NBEV Margin**.

It is calculated as the ratio of the NBEV Dollar to the APE, representing the **expected profit per dollar of premium collected**:

$$

$$

Despite this, the NBEV Dollar Amount is used as the KPI, rather than the margin.

The NBEV dollar KPI can be determined in two ways:

* **Bottom Up Approach**: Put Budget APE into prophet and calculate the NBEV Dollar
* **Top Down Approach**: Arbitrarily choose Budget NBEV Margin and multiply by sales to get NBEV Dollar
* Bottom Up Approach is much better as it is transparent and easily explainable

## **Insurance Operating Results**

**Insurance Operating Results** (IOR) is an industry term used to refer to the **Operating Profit** BEFORE tax.

It can be roughly understood as the sum of two components:

$$

$$

IOR 
#NAME?
#NAME?
= "Net" Premium - Expenses

Selling & Management Expense
Expense overrun
Loading > Budgeted Expense
Actual
Cannot consistently blow your assumptions

Operating > Something that management control EG. Inflation cannot be controlled
Attribute Performance to who > Management or out of their contorl

For BP purposes, it has been aligned that the allocation


Based on confidence interval, risk appetite

Payback period
How fast you can recoup back this NB strain

About reaction - how to manage it
KPI is about the state of the company

Forecast is if you are on track then is ok
Bottom up to match group number

EV can be manipulated b assumption
no point writing a lot of business with little value
Should be set then bottom up to see if can

Problem with Income is that they dont know what they want

# **New Business Embedded Value** (NBEV)

## Drivers

Drivers -- big things that can affect NBEV
Volume
Product Mix > Mix of the different lines of products (Life/Health/GI)
Policy Mix > Mix of the different policies within each category
Economic Assumptions > RFR, CoC

## Attribution

Movement from Budget to Actual -- breaking down the movements to specific drivers
Same method as life con profit attribution -- Actual - Expected, once accounted use actuals

NBEV = Sales * Margin
NBEV = Total Sales * Sales Mix * Margin
Margin is affected by Policy Mix & RFR/CoC

NBEV due to Sales Volume = (Actual Sales - Budget Sales) * Budget Margin
NBEV due to Sales Mix = (Actual Mix - Budget Mix) * Total Actual Sales * Budget Margin

*NBEV due to Policy Mix = (YE22 Actual Mix, RFR & COC - YE22 Budget Mix, RFR & COC) * Actual Sales 
NBEV due to CoC = (YE22 Actual Mix & RFR Margin - YE22 Actual Mix, RFR & COC Margin) * Actual Sales
NBEV due to RFR = (Actual Margin - YE22 RFR Margin) * Actual Sales

* It is not possible to calculate the second component of Policy Mix -- YE22 Budget Mix, RFR & CoC
-- There is no way to do a bottom's up approach for this
Possible to do runs for CoC and RFR using the current month MPF with different assumptions
Thus, this is usually calculated as a balancing item
In other words, we compute Budget, Actual and each other component -- the difference (balance) Thus must be attributed to policy mix

Budget to Actual
Actual June Margin - Expected Drivers = Actual Dec Margin
Actual Dec Margin - Buffer = Budget Dec Margin

Surplus is net assets > any excess of asset and liability
In theory, all surplus can be used freely by the shareholders -- they can keep for buffer or they can distribute to shareholders
However, not all surplus is free because some extra capital is used as Required Capital
Thus, this required capital earns the rate backing surplus (While the reserves earn the rate backing liability)

Net Cashflow also earns interest
Negative Interest is also considered -- borrow money?
Last period discounting is slightly different -- Profit occurs at the beginning of period, everything else at the end of period


NBEV = PROFIT AFTER SOLVENCY (DISC_SPROF_A)

PAR NBEV IS DIFFERENT

1. Mix -- Affects individual groups
2. RFR -- Affects all policy

TU have higher margin because expenses are low.
mix is important
Once replace wont sell anymore, but can top up

About 10% of the base margin is ok
Some months swing a lot because high margin product (Provenance)

SA Factor
Rider and Term


Reserve affects the speed of profit:
lower RFR -> higher reserve -> slower profit emergence means profit will realize at late duration rather than early duration -> slower profit emergence means discounting effect on profit would be stronger (i.e. lower PVFP) -> lower NBEV

Bank sells alot of SP
PD -- not part of Bank
Agency, RFS -- part of income
PD - HNW
RFS - API, general population

Private Credit -- Funding Society
Counterparty Risk only

NBEV is EV for new business
However, ANW at time 0 is 0 so it is actually just VIF
ANW is a measure how much this block of business has already earned, since the business just incepted, the ANW is 0

NBEV Adjustments
Campaign Costs
Costs that were NOT considered inside the MPF
They should still reduce NBEV accordingly



# EV AoM Variance

| Step | First Year Lapse | First Year Death | Portfolio
|  1   |         Y        |         Y        | All
|  2   |         X        |         Y        | All
|  3   |         X        |         X        | All
|  4   |         X        |         X        | Policies that actually Lapsed
|  5   |         X        |         X        | Policies that actually Died

Operationally remove FY Lapse/Death done by applying a 100% shock in the first year

Step (2) - Step (1): Expeted Lapse Impact
Step (3) - Step (2): Expected Death Impact
Step (4): Actual Laspe Impact
Step (5): Actual Death Impact

Lapse Variance = Expected Lapse Impact - Actual Lapse Impact
Death Variance = Expected Death Impact - Actual Death Impact

For ANW, the amount is quantified via change in Reserve (MCL).

Need to consider the variance in the actual claims paid as well 
expected: extract from Prophet
Actual: from financial statement
 Variance: difference between the two

# To compare two positions

YE22 M12 Position (WITH FY LAPSE AND DEATH TURNED OFF)
YE23 M0 based on YE22 RFR curve unwinded one year

Both positions SHOULD lead to the same results. Any difference is likely due to unexplained differences in the MPF

Should be able to match NOP at an individual level
