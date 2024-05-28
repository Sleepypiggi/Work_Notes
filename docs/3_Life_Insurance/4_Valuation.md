# **Life Insurance Valuation**

Valuation in Insurance has the same meaning as it does in finance - it is to **determine the economic value** of a business, typically via finding its **present value**.

Finance valuation typically focuses on valuing *assets* in order to determine an approriate stock price while Actuarial valuation focuses on valuing *liabilities* to determine the required reserve for the policy.

Unlike finance, valuation in insurance is a heavily regulated process with a fixed method of doing so. It is typically done by considering the **difference in the present value of the expected cash inflows and outflows** (NPV) from the *insurer's perpective*.

| Cash Inflows | Cash Outflows |
|:-:|:-:|
| Premium | Insurance benefits & Expenses |

## **1. Singapore Regulation**

Valuation in Singapore is governed by the [Insurance (Valuation and Capital) Regulations 2004](https://sso.agc.gov.sg/SL/IA1966-S498-2004) which is part of a larger set of regulations known as the [Insurance Act](https://sso.agc.gov.sg/Act/IA1966).

The methodology for valuation is described in sections 20 and 20A of the 2004 regulation for valuation on a Net (after reinsurance) and Gross (before reinsurance) basis respectively.

### **1.1 Prescribed Methodology**

For non-participating policies,

``` x
Policy Liability 
= Expected Future Payments (Benefits & Expenses)
- Expected Future Receipts
+ Provision for Adverse Deviation
```

For participating policies,

``` x
Policy Liability 
= Expected Future Payments
- Expected Future Receipts
+ Provision for Adverse Deviation
+ Future Allocations of Bonus/Surplus
```

For unit-linked policies,

``` x
Policy Liability = Unit Reserves + Non-unit Reserves

where
Unit Reserves = Value of underlying assets
Non Unit Reserve = Expected Future Payments - Expected Future Receipts + Provision for Adverse Deviation 
```

Notice that all methods are *at least* the sum of the `Net Expected Payments` and `Provision for Adverse Deviation`.

## **1.2 Present Value**

All values in the previous section are the **Present Values** of the respective cashflows, calculated using the [Discounted Cashflow Method](https://en.wikipedia.org/wiki/Discounted_cash_flow).

For non-participating and unit-linked policies, the discount rate to use is the **Risk Free Rate** (RFR), which can be obtained from the government yield curves. RFR is used to discount as these cashflows are *guaranteed* and thus *Risk Free*.

For participating policies, the discount rate to use is the **Best Estimate Investment Return** (BEIR), which is calculated by the insurer based on what they expect the assets backing the policy to earn. Since it has *non-guaranteed benefits* depending on the *performance of its underlying assets*, we should use return of the underlying assets for discounting.

The *timing* of the cashflows also matters when it comes to discounting. If we assume cashflows occur at the start of the period, they will be discounted slightly less than those that occur at the end.

In general, `premium`, `commissions` and `expenses` occur at the *start* of the period as these cashflows must occur for the policy to remain in force for the remaining of the period. Similarly, `maturity` cashflows occur at the start as the policy is in force till the end of the policy period (inclusive). All other cashflows are typically assumed to be at the *end* of the period.

## **1.3 Expected Value**

All cashflows in a typical life insurance policy are *contingent* on the policyholder lapsing, dying or neither during the policy term.

As such, we should not consider the absolute value of these cashflows but rather the **Expected Values** at each period. This is done by multiplying the cashflow by a *probability* of (not) Lapsing (**Lapse Rate**) and/or Dying (**Mortality Rate**).

Additionally, there are some values that we *do not know for sure* of at the time of valuation such as Expenses or Bonuses as they are dependent on the economic environment at the time. For these cashflows, we make **assumptions** about how they would by assuming they would be grow based on a certain *rate*.

Thus, the Present Value of the Net Expected Payments is also referred to as the **Best Estimate Liability** (BEL). This is because the assumptions we use should be our *best guess* about how the future will play out, which is based on our *recent experience* of the policyholders.

### **1.3a Valuation Assumptions**

<!--
Management Expenses
Distributon Expenses
Inflation
Mortality 
Morbidity
Lapse Rates
Bonus Rates
-->

Regulators don't generally like negative reserves, as including credit for them reduces the overall reserve amount (so the insurance company has less backing assets) and it is imprudent, as the policyholder in the situation above may realise their position and lapse their policy (so the insurance company never actually receives the positive premiums).

Each country has their own set of regulations regarding how reserves should be calculated and how much capital should be held
o	Insurance (Valuation and Capital) Regulations 2004
o	Notice 133 Valuation and Capital Framework for Insurers
•	A fully qualified actuary must sign off on the reserves to attest that the reserves have been properly determined in adherence to the relevant guidelines
o	Remember that the goal is NOT to prevent insurance companies from going insolvent but rather to protect policyholders from the consequences of insolvency

## **1.4 Provision for Adverse Deviation**

Calculating liabilities based on BEL alone assumes that our assumptions are 100% correct, which is almost never in practice.

If our actual experience is *worse* than our assumptions, then the reserve for that period will NOT be enough to cover claims in that period, leading to bankruptcy.

In order to avoid that scenario, insurers are required to hold some *additional capital* as a buffer, formally known as **Risk Margin** or **Provision for Adverse Deviation**.

BEL + PAD is calculated by *shocking* each of the assumptions used by a PAD factor. Note that the shock applied must result in a *worse* situation for the insurer (higher reserve). This means that the shock could be an increase or decrease (not strict) as *certain* assumptions have an ambiguous effect on reserves.

For instance, increasing Lapse rates increase both Surrender/Death Benefit (Outflows) & Premiums (Inflows). Thus, there is a need to *test* which direction to apply the shock.

## **1.5 Minimum Condition Liability**

The BEL for participating policies captures both the Guaranteed and Non-Guaranteed benefits. This may not be an "accurate" representaton of the liability as the non-guaranteed benefits may not occur at all.

Thus, we instead consider ONLY the guaranteed benefits of a participating policy - which forms the lower bound (minimum) of the liability. Similar to before, since only guaranteed benefits are considered, we should use the RFR for discounting. This is also commonly referred to as the **Minimum Condition Liability** (MCL) of a participating policy.

> Note that there is no such thing as MCL for a non-participating products as they only have guaranteed benefits - there is no minimum.

## **2. Modelling**

Given the large number of policyholders, it is not feasible to manually calculate the liability. Thus, actuarial models are built to automatically calculate the values for us.

There are many different types of Life Insurance products, each with their own distinct features. Thus, each type of product needs to have its own model.

Similarly, each product has many different policyholders, each with their own unique information - `Sex`, `Age`, `Premium`, `Sum Assured` etc. These are usually called **Model Point** data as they are used as inputs into the model.

For a *single* model point, Excel can be easily used to calculate the liability for checking purposes. However, Excel is not suited to repeat calculations for multiple model points (although possible).

Most major insurers would use enterprise level software to calculate the liability, such as **FIS Prophet** or **Moody's AXIS**. These software have the capability to calculate the liability for multiple model points and multiple products at once.

In general, these software accomplish this by considering three sets of inputs:

* **Global Inputs** - Assumptions that are constant across ALL models (EG. Discount Rate)
* **Parameter Inputs** - Assumtions that are unique to each model (EG. Lapse Rates)
* **Model Point Inputs** - Policyholder information

### **2.1 Modelling VS Valuation**

Some companies make a clear distinction between the two - Modelling is focused on building and mainting the models, while Valuation is concerned about preparing inputs and intepreting output.

Regardless of a split or not, the two functions are heavily intertwined with one another - it is important to know both sides of the process.

Jerram, [6/1/2023 6:22 pm]
Life Insurance modelling is a Cash Flow Model that is dependent on a Statistical Model that produces the experience studies

Jerram, [6/1/2023 6:23 pm]
Mortality risk is much more stationary and Low variance

Jerram, [6/1/2023 6:23 pm]
Room for atatsical modelling but not much more improvement or competitive advantage

Jerram, [6/1/2023 6:24 pm]
Persistency modelling is much less explored

Jerram, [6/1/2023 6:26 pm]
Lapses and Surrenders are much more volatile than Mortality

Jerram, [6/1/2023 6:27 pm]
Modelling them more accurately reduces income volatility through reserves 

Less duration mismatch and more effective hedges which could improve investment income

Jerram, [6/1/2023 6:31 pm]
Unique Risks, not a lot of data (P&C) > Stochastic Modelling

Predictive Modelling, a lot of homogenous data

# **Life Insurance Valuation**

Valuation in Insurance has the same meaning as it does in finance - it is to **determine the economic value** of a business, typically via finding its **present value**.

Finance valuation typically focuses on valuing *assets* in order to determine an approriate stock price while Actuarial valuation focuses on valuing *liabilities* to determine the required reserve for the policy.

Unlike finance, valuation in insurance is a heavily regulated process with a fixed method of doing so. It is typically done by considering the **difference in the present value of the expected cash inflows and outflows** (NPV) from the *insurer's perpective*.

| Cash Inflows | Cash Outflows |
|:-:|:-:|
| Premium | Insurance benefits & Expenses |

## **1. Singapore Regulation**

Valuation in Singapore is governed by the [Insurance (Valuation and Capital) Regulations 2004](https://sso.agc.gov.sg/SL/IA1966-S498-2004) which is part of a larger set of regulations known as the [Insurance Act](https://sso.agc.gov.sg/Act/IA1966).

The methodology for valuation is described in sections 20 and 20A of the 2004 regulation for valuation on a Net (after reinsurance) and Gross (before reinsurance) basis respectively.

### **1.1 Prescribed Methodology**

For non-participating policies,

``` x
Policy Liability 
= Expected Future Payments (Benefits & Expenses)
- Expected Future Receipts
+ Provision for Adverse Deviation
```

For participating policies,

``` x
Policy Liability 

= Expected Future Payments
- Expected Future Receipts
+ Provision for Adverse Deviation
+ Future Allocations of Bonus/Surplus
```

For unit-linked policies,

``` x
Policy Liability = Unit Reserves + Non-unit Reserves

where
Unit Reserves = Value of underlying assets
Non Unit Reserve = Expected Future Payments - Expected Future Receipts + Provision for Adverse Deviation 
```

Notice that all methods are *at least* the sum of the `Net Expected Payments` and `Provision for Adverse Deviation`.

## **1.2 Present Value**

All values in the previous section are the **Present Values** of the respective cashflows, calculated using the [Discounted Cashflow Method](https://en.wikipedia.org/wiki/Discounted_cash_flow).

For non-participating and unit-linked policies, the discount rate to use is the **Risk Free Rate** (RFR), which can be obtained from the government yield curves. RFR is used to discount as these cashflows are *guaranteed* and thus *Risk Free*.

For participating policies, the discount rate to use is the **Best Estimate Investment Return** (BEIR), which is calculated by the insurer based on what they expect the assets backing the policy to earn. Since it has *non-guaranteed benefits* depending on the *performance of its underlying assets*, we should use return of the underlying assets for discounting.

The *timing* of the cashflows also matters when it comes to discounting. If we assume cashflows occur at the start of the period, they will be discounted slightly less than those that occur at the end.

In general, `premium`, `commissions` and `expenses` occur at the *start* of the period as these cashflows must occur for the policy to remain in force for the remaining of the period. Similarly, `maturity` cashflows occur at the start as the policy is in force till the end of the policy period (inclusive). All other cashflows are typically assumed to be at the *end* of the period.

## **1.3 Expected Value**

All cashflows in a typical life insurance policy are *contingent* on the policyholder lapsing, dying or neither during the policy term.

As such, we should not consider the absolute value of these cashflows but rather the **Expected Values** at each period. This is done by multiplying the cashflow by a *probability* of (not) Lapsing (**Lapse Rate**) and/or Dying (**Mortality Rate**).

Additionally, there are some values that we *do not know for sure* of at the time of valuation such as Expenses or Bonuses as they are dependent on the economic environment at the time. For these cashflows, we make **assumptions** about how they would by assuming they would be grow based on a certain *rate*.

Thus, the Present Value of the Net Expected Payments is also referred to as the **Best Estimate Liability** (BEL). This is because the assumptions we use should be our *best guess* about how the future will play out, which is based on our *recent experience* of the policyholders.

### **1.3a Valuation Assumptions**

<!--
Management Expenses
Distributon Expenses
Inflation
Mortality 
Morbidity
Lapse Rates
Bonus Rates
-->

Regulators don't generally like negative reserves, as including credit for them reduces the overall reserve amount (so the insurance company has less backing assets) and it is imprudent, as the policyholder in the situation above may realise their position and lapse their policy (so the insurance company never actually receives the positive premiums).

Each country has their own set of regulations regarding how reserves should be calculated and how much capital should be held
o	Insurance (Valuation and Capital) Regulations 2004
o	Notice 133 Valuation and Capital Framework for Insurers
•	A fully qualified actuary must sign off on the reserves to attest that the reserves have been properly determined in adherence to the relevant guidelines
o	Remember that the goal is NOT to prevent insurance companies from going insolvent but rather to protect policyholders from the consequences of insolvency

## **1.4 Provision for Adverse Deviation**

Calculating liabilities based on BEL alone assumes that our assumptions are 100% correct, which is almost never in practice.

If our actual experience is *worse* than our assumptions, then the reserve for that period will NOT be enough to cover claims in that period, leading to bankruptcy.

In order to avoid that scenario, insurers are required to hold some *additional capital* as a buffer, formally known as **Risk Margin** or **Provision for Adverse Deviation**.

BEL + PAD is calculated by *shocking* each of the assumptions used by a PAD factor. Note that the shock applied must result in a *worse* situation for the insurer (higher reserve). This means that the shock could be an increase or decrease (not strict) as *certain* assumptions have an ambiguous effect on reserves.

For instance, increasing Lapse rates increase both Surrender/Death Benefit (Outflows) & Premiums (Inflows). Thus, there is a need to *test* which direction to apply the shock.

## **1.5 Minimum Condition Liability**

The BEL for participating policies captures both the Guaranteed and Non-Guaranteed benefits. This may not be an "accurate" representaton of the liability as the non-guaranteed benefits may not occur at all.

Thus, we instead consider ONLY the guaranteed benefits of a participating policy - which forms the lower bound (minimum) of the liability. Similar to before, since only guaranteed benefits are considered, we should use the RFR for discounting. This is also commonly referred to as the **Minimum Condition Liability** (MCL) of a participating policy.

> Note that there is no such thing as MCL for a non-participating products as they only have guaranteed benefits - there is no minimum.

## **2. Modelling**

Given the large number of policyholders, it is not feasible to manually calculate the liability. Thus, actuarial models are built to automatically calculate the values for us.

There are many different types of Life Insurance products, each with their own distinct features. Thus, each type of product needs to have its own model.

Similarly, each product has many different policyholders, each with their own unique information - `Sex`, `Age`, `Premium`, `Sum Assured` etc. These are usually called **Model Point** data as they are used as inputs into the model.

For a *single* model point, Excel can be easily used to calculate the liability for checking purposes. However, Excel is not suited to repeat calculations for multiple model points (although possible).

Most major insurers would use enterprise level software to calculate the liability, such as **FIS Prophet** or **Moody's AXIS**. These software have the capability to calculate the liability for multiple model points and multiple products at once.

In general, these software accomplish this by considering three sets of inputs:

* **Global Inputs** - Assumptions that are constant across ALL models (EG. Discount Rate)
* **Parameter Inputs** - Assumtions that are unique to each model (EG. Lapse Rates)
* **Model Point Inputs** - Policyholder information

### **2.1 Modelling VS Valuation**

Some companies make a clear distinction between the two - Modelling is focused on building and mainting the models, while Valuation is concerned about preparing inputs and intepreting output.

Regardless of a split or not, the two functions are heavily intertwined with one another - it is important to know both sides of the process.

This is not very easy question to answer, and I'm not great at explaining things but I'll try my best.

The two questions tie hand in hand. You are mixing up the "reserve" with the "liability".

The reserve is the present value of future liability minus the present value of assets. For simplicity's sake, I will ignore expenses and profits, so the liability is just the claim payments (outgo) and assets are premium payments (inflow). Another perhaps obvious thing is, a larger (more positive) reserve is "bad" for the insurer in the sense that they have to find ways to get more money to pay this off.

I tend to think of the reserve = 0 at t = 0 as a pricing philosophy, where you should charge the premium such that it equals the liability, net of expenses and profits. And the 0 reserve at time 0 is a trivial product of this philosophy.

For the U-shaped reserve, imagine you are an insurer and you sold a whole life policy to an 18-year-old, and the premium is $P per year until they die, and the policy pays $F when they die.

EDIT: I'm wrong. I was wrong because in my example, the good years in the beginning must suggest all the years after that will be equally as bad. (eg. if I gained $50 in first 2 years, then in the rest of the policy life time, I am expected to lose $50 so that at time 0 I break even, ignoring interest).

here's the (what I think) correct explanation:

Now imagine you sold many policies of the same kind. The early years' future claim payments doesn't decrease a lot, since the policyholder is healthy (claim payments are back-loaded), but the future premiums decrease more or less linearly. This means that the PV(liability)-PV(premiums) will increase in early years. And decrease in later years because the policies's liability decrease per year gets larger and larger.

This is perhaps an overly simplistic answer but I hope I got the idea across.

For the second part, the reserve pattern with policy duration is hump shaped because the expected present value of the remaining future benefits decrease slowly at early durations ( as the overall probability of claiming under the policy only reduces by a relatively small amount), but increasingly rapidly at later durations ( as the probability of a claim being made under the policy decrease quickly to zero as the end of the term approaches). In contrast, the expected present value of the future premiums declines at an almost linear rate ( assuming level premiums) with increasing policy duration.


The reserve = 0 at time 0 is the result in net premium valuation because the net premium is set at the level where PV NP = PV Benefits. Under the real life situation (esp. low interest rate environment), it is possible to have NP capped by the gross premium, and the insurer needs to set up premium deficiency reserve at policy inception.

    reserve is pv death Ben less pv prem. If pv death Ben is higher than pv prem at the start of the policy, it would be unprofitable. The company can pay for the death benefit that happens in year one, because they sell a hundred policies and take in a hundred premiums in year one, but only one person dies, so they redirect premiums from multiple policies to pay for the one claim in year one.

    term life has level premiums, but increasing mortality costs. In early years, the excess premium goes to building a reserve. In later years, the reserve is used to pay for death benefits being higher than premiums.

This explanation is a bit theoretical, but is fundamentally how it works. This ignores expenses, profits, etc, which add a bit of complexity.

Life Insurance & Annuities for Actuaries
Life Contingencies
Overview
	As mentioned earlier, Life Insurance is extremely long term – Actuaries in this field mainly deal with cashflow projections
	Each policy has a different feature which results in different Per-Policy Cashflows
	These cashflows are contingent on a certain event happening (Surviving, Death or Lapse). Thus, it is not appropriate to consider the raw cashflows but rather the In-Force (Expected) Cashflows using the Number of Policyholders (NOP)
	Additionally, these cashflows occur far into the future. Instead of considering their raw values, we consider their present value to properly account for the time value of money

Number of Policyholders (NOP)
	Consider a population of 1000 similar policyholders. We know the following information:
	Number of Policyholders alive at the start of the period
	Number of Policyholders who Lapsed during period
	Number of Policyholders who Died during period
	Number of Policyholders who Matured during period
	Number of Policyholders alive at the End of the Period
	With this information, we can simply multiply the respective cashflows by the number of policyholders that triggered that cashflow:
	Premium*NOP Alive at period start
	Death Benefit*NOP Died during period
	Surrender Benefit *NOP Lapsed during period
	Maturity Benefit*NOP Mature during period
	Assuming that the Cashflows for all the policyholders are the same
	In practice, we typically build models to project one policyholder at a time. Thus, we consider a starting population of 1
	This means that subsequent NOP cannot be greater than 1 or smaller than 0 – like a probability rate. Thus, in-force cashflows are like Expected Cashflows
	However, we will not know the actual NOP till the period has passed. Thus, we will need to project these NOP by analysing our experience & using Survival Models

Experience Studies
	We need to make several assumptions about the future to make our results more concrete. We typically make assumptions on:
	Decrements → Rates that remove the policyholder from the population (Death, Lapse, Maturity)
	Utilization → Rates that DO NOT remove the policyholder from the population (Partial Withdrawal, Premium Holiday etc)
	Other Global Variables → Interest rates, Expense etc
	Insurers typically analyse their past data through Experience Studies to obtain assumptions that best reflects their experience to predict the future. The results of these studies represent snapshots in time – thus periodic reviews must be conducted to fully make use of new experience
	All of these assumptions pose a risk to the insurer. If our actual experience is worse than what we assumed, then our calculations are insufficient to cover costs etc
	On the flipside, if our actual experience is better than assumed, this means that our calculations were excessive thus the excess reserves are released as profits
	Anything can be done in Life Insurance, if we expect it

Sales Channel increase lapse
Direct channle higher risk because they know their risk better and willingly join the pool
Agent lower risk because they go to client

High interest rates are great for the industry because most of the industry is in Bonds
Investment incoming should be booming if held to maturity

Potential issue is disintermediation - if interest rates rise, then products that are crediting low rates will be unexpectedly lapsed (from the company's perspective) lapsed as consumers just go to buy directly from the market with booming rates
Companies will need to liquidate their holdings to pay off these lapsers
However, since market value of these assets falls, then this will lead to a loss for them

Insurance uses ALM so PV of liability and PV of bonds fall together, no impact on existing business
New business will be repriced to reflect new environment

Insurers focus on asset liability matching rather than pure price
When interest rates increase, both the PV of liability and bond price decreases together, thus they offset each other

PA Policy Asset
PL Policy Liability
PPT is premium payment term

Cant keep changing assumptions also

Experience, adjust credibility plus loading


Inflation tough because they represent rising cost but there may be regulations which makes it hard to pass down this cost to consumers

Insurance companies take up good debt to reduce the risk charge - no need to hold extra investments and can reduce expenditure, protecting bottom line


 Survival Models
	Choose a Valuation date – Any date after policy inception and before policy maturity
	Our implicit assumption is that the policyholder is alive at the date – Thus the NOP on the valuation date is always 1
	Using our assumptions about Mortality & Lapse, we can model the NOP:
	We need to calculate how many people Die or Lapse each period
	We do this by multiplying the NOP at period start with the probability of Dying or Lapsing WITHIN THAT PERIOD respectively
	NOP_End=NOP_Start-NOP_Surrender-NOP_Death-NOP_Maturity
	Naturally, the NOP for a period end is the NOP for the next period start
	The tricky part is determining the probability of Dying or Lapsing:
	We usually assume a certain percentage of people Die or Lapse each year
	However, valuation is typically done in monthly time periods
	We thus need to adjust the given rates:
	Both Lapse and Mortality are decrements – in other words they are discount rates, not interest rates 
	We can convert them using → (1-Monthly)=(1-Yearly)^(1/12)
	There is a more theoretically correct method to do this using survival rates, but the result is identical
	The NOP Death and Lapse dictate the total number of people who die or lapse in a period assuming all else constant. When assuming both together, it becomes complicated:
	If you already died, then you cannot lapse, vice versa. This means that the NOP of Death and Lapse should be much lower than they are
	There are theoretical ways to overcome this, but in practice we usually assume that people die first or lapse first, which affects your NOP calculation
	Policies mature at the start of the period, so the NOP Maturity is simply the starting NOP of the first period after the policy term (IE NOP of last the period in policy term)

Mortality Tables
	Each mortality table typically has two forms – Select & Ultimate Mortality
	The Select table is used for new business while Ultimate is used for existing business
	Select Mortality is LOWER than Ultimate Mortality → Less likely to die
	This is because new business has gone through medical underwriting and should be healthier, thus should have lower mortality (All else equal)
	Once the policy has been in-force for 1-2 years, the policy will then use the Ultimate Mortality table which has a higher mortality (All else equal)

Interesting Impact of Decrements
	Consider a base case of decrements and cashflows
	If we increase decrements in the early years, then naturally the expected outflow cashflows in the early years will increase as well
	However, because more policyholders left the pool early on, there will be fewer to leave the pool in the future, causing a decrease in expected outflows in the future
	Conversely, assuming lower decrements early on will lower expected outflows in the early years while increasing expected outflows in the future




Life Pricing – Goal is to cover the expected losses and achieve some level of profit

Main factors to price based on:
Gender
Age
Smoking Status
Underwriting Loading Factors like Health Conditions, Foreigners, Occupation etc


Life Insurance uses VNB, EV NBS etc
Reserve = Claims – Prem
Negative is good, means we are collecting more premium than claims
Reserve only affects tge timing of profit
Under RBC2, C1 risk charge is 95%VAR (~2SD) 
Sweet Spot is to hold 90% (~1SD) as PAD
Don’t hold too much as PAD because opportunity cost of capital
Don’t hold too little because regulator will challenge
If set C1 = PAad, its an accounting trick to artificially increase the CAR of the company
C1 and Pad are complement of each other

EV = Value of In Force – Adjusted Net Worth
Value in force = Future Profits
Adjusted Net Worth ARE THE NON VALUABLE items

History of EV > Hostile takeovers in the 1900s
People unsure how to properly measure profitability

Come up with EV as a way to measure the profitability
Metric to shareholder since the share price is often not a reliable measure
IFRS17 too aligned with the banks and Australian profit thingy

GWP > Volume
EV > Profitability

NBEV > New business
NBEV_TU > Minus top up from ILP holders
Grwoth oriented metric

No point to build a new prophet system
Existing systems already use prophet, people know how to use prophet
Very hard to break into the market

Regulations in insurance exist because an information asymmetry exists between the seller and buyer of insurance products. Buyers don't know if the price is appropriate or the exact extent of covered loss events. Regulators bridge this gap.


