## **Unit Linked**


A **Unit-Linked** Policy is one that **invests the premiums** into **unit trusts** of professionally managed **mutual funds** of the policyholder's choice. This is why they are also commonly referred to as an **Investment-Linked Policies** (ILP).

Each policy has a **unit account** that stores the purchased units. The account value is the **total NAV** of the units at the time.

The unit account is conceptually similar to the cash account of a UL policy:

1. Premiums are used to purchase units of chosen funds
2. Units are sold to pay off any insurance or expense charges

The account value can be accessed via a withdrawal or loan, through the **sale of the units** at the prevailing NAV. Similarly, if the account value **reduces to zero** due to poor market conditions, the policy will **lapse**.

There are generally two types of ILPs, which determines how the death benefit is structured:

<center>

|         **Protection Focused**          |             **Investment Focused**              |
| :-------------------------------------: | :---------------------------------------------: |
|             Has sum assured             |            Does NOT have sum assured            |
| Higher of account value and sum assured | Higher of account value and total premiums paid |

</center>

The key selling point of an ILP is that it is able to **generate high returns**, allowing it to **overcome inflation** which has typically plagued the other types of insurance policies. 

Unlike all other forms of insurance, there are **NO investment guarantees**. The policyholder bears ALL the **investment risk**. If the underlying funds perform badly, the account value could decrease and result in a loss for the policyholder.

This section will go over commonly found features in unit-linked products.

### **Premium Allocation**

Premium Allocation refers to what **proportion of premiums** are used to **purchase units**.

There are two commonly taken approaches, each differing in how the premium is allocated in the **first few years** of the policy:

<center>

|     **Front End Loaded**     |      **Back End Loaded**      |
| :--------------------------: | :---------------------------: |
|  Lesser than 100% allocated  |    Exactly 100% allocated     |
| No minimum investment period | Has minimum investment period |
|     No surrender charge      |     Has surrender charge      |

</center>

!!! Info

    Loading refers to the **additional amount** added to the **pure premium** to cover items such as expense, profit, tax etc.

The **cost of setting up a unit-linked policy** is generally higher than an otherwise non-unit linked policy due to all the costs associated with setting up a unit account.

As with all other policies, the insurer **recovers these costs over time**. Thus, the problem lies with policyholders who **lapse their policy before** the insurer can recover the full cost. This is more pronounced for unit linked policies given the investment nature of the product.

In a **front-end loaded** approach, the insurer **recovers the cost beforehand**, ensuring that the costs are mostly recovered early on regardless of whether or not the policy is lapsed.

$$
    \text{Allocated Premium(t)} = \text{Premium(t)} \cdot \text{Allocation Rate(t)}
$$

In a **back-end loaded** approach, the insurer will recover the remaining cost only when the insured lapses their policy. This is done via a **Surrender Charge**, which reduces the surrender value of the policy by a **specified proportion**.

$$
    \text{Surrender Value(t)} = \text{Fund Value(t)} \cdot \text{Surrender Charge Rate(t)}
$$

In both cases, the upfront costs will be **recovered over time** as long the policy remains in-force. Thus, the loading amount gradually decreases:

1. **Front Loaded**: Premium allocation gradually increases back to 100%
2. **Back Loaded**: Surrender charges gradually decrease to zero

!!! Note

    The period where surrender charges are applicable is typically known as the **Minimum Investment Period** or **Surrender Charge Period**.

    This is becaused it is assumed that the policyholder will not lapse during this period so as to avoid the surrender charge.

In both cases, premium allocation rates tend to **increase above 100%** after a certain period, incentivising the policyholder to **retain their policy** to get the additional value. 

The premium allocation schedule is typically **non-guaranteed**, but most insurers *floor* the allocation rates at 100%.

!!! Info

    MAS307 mandates that the term "Premium Allocation Rate" cannot be used in any communication to policyholders.

    This is because it implies that the allocated amount will be used to purchase units. However, in reality, the premiums are subject to further charges (as described below).

### **Premium Charges**

Premium Charges refer to the charges applicable to the **purchase of units**. The purpose of the charge is to **compensate the distributor** of the units, akin to a commission fee.

They are typically applied in the form of a **percentage reduction** of the amount of available premium to purcahse units:

$$
    \text{True Premium} = \text{Premium(t)} \cdot [1 - \text{Premium Charge(t)}]
$$

More generally, these charges come in one of two forms:

* **Sales Charge**: Front end load applied to the transaction volumes
* **Bid-Offer Spread**: Difference between bid and offer prices

Both items are typically represented as a **percentage** (EG. 5%).

!!! Note

    Bid Offer Spreads are a general financial concept:

    * **Bid Price**: Price that fund manager will bid for a unit (Policyholder sell price)
    * **Offer Price**: Price that the fund manager will offer for a unit (Policyholder buy price)

    The bid price will **always be lower** than the offer price, ensuring that there is a spread. This is to ensure that there is profit to be earned to incentivise distributors to trade the units.

### **Top Ups**

Apart from the normal premium schedule, policyholders can make **adhoc top-ups** into the policy.

Top-ups are subject to premium allocation and premium charges, but may have a different rate compared to Single/Regular premiums.

### Bonus

Welcome
Loyalty

Welcome Bonus hits the unallocated premium, negative unalloc prem
Cost of bonuses


Whenever there are charges posted to the policy, it will **sell units** to cover the charges. On top of the typical insurance related charges, they also contain **investment related charges** (Fund Management Charges, Expense Ratios etc).

 *Regardless* of the investment performance, the insurer will take a **fixed spread** from the investment.

> Note that it is often difficult to determine the actual price of the units used for allocations or charges as there is often a delay due to processing. The transaction may only occur a few days later, thus using the unit price then rather than when it was initiated.

The death benefit of the policy is the typically the **higher of the Account Value or a Capital Guarantee**, similar to Endowment Insurance. The NAAR of the policy is the Capital Guarantee less the Account Value. Thus, if the account value is sufficiently high, the **NAAR will be negative** and there will be **no mortality charges** on the policy.

The surrender benefit of the policy is only the account value.

$$
\displaylines{
Death~Benefit = Max (Account~Value, Capital~Guarantee) \\
NAAR = Capital~Guarantee - Account~Value
}
$$



### **Mortality Charge**

### Annual Management Charge

### **Premium Holiday**

<!-- 

### **Premium Holiday**

This self-sustaining nature of the policy means that if policyholders choose not to pay premiums anymore, the policy will still be in-force as the necessary insurance charges are still being paid for by the fund value

If the policy is on premium holiday during the first 10 policy years, we will deduct a premium
holiday charge on a monthly basis from the account value

Premium holiday during MIP have charges
Stop paying after grace period
policy will not lapse immediately > Will enter premium holiday
Provided that fund value is sufficient
Cease after pay again
but charges applicable during MIP

-->


### **Net Amount at Risk**

The Death and Surrender Benefit are **mutually exclusive** - the insurer will only end up paying only one in the end.

Thus, we can think about the death benefit at every period as the combination of the **Cash Value** of the policy and a **one period renewable term policy**. The coverage of this term policy is known as the **Net Amount at Risk** (NAR) and is the difference between the Death Benefit and the Cash Value. It represents the amount of money the insurer has to pay in the event of a claim, hence is *at risk* to the insurer.

$$
Death~Benefit = Cash~Value + Net~Amount~At~Risk
$$

<!-- Obtained from Partners Advantage Blog -->
![Permanent NAAR](Assets/1.%20Life%20Products.md/Permanent%20NAAR.png)

The premium for this term policy is known as the **Cost of Insurance (COI)**. It is the product of the **coverage of the policy** (NAAR) and the **cost per unit coverage** (COI Rate). It is typically some function of the mortality experience.

$$
Cost~Of~Insurance = COI~Rate * Net~Amount~At~Risk
$$

Regulation says can’t recognise negative reserve

Par Non Par
Reserve = Liability so must floor

ILP
Reserve = Unit + Non Unit Reserve (Liability)

As long as total non negative, can already > Can recognise negative non unit reserve

Strain is due to setting up reserves and expenses etc

Because insurance is backend loaded, recover profits over time

Worsened for modern ILP because most are super backended

No allocated premium
Minimal fee income in the first year

But need pay out expenses reserve and bonus units etc

ILP Bonus Unit
Most common RP ILP these days should not have any COI

GTD Benefit is 105% of premiums 
Pay premium 
Get welcome bonus
Welcome bonus higher than 5%
Thus SAR should be 0

No COI, only got Policy Fee, FMC

Negative reserve interaction with Capital is weird

Negative reserve > Offset your capital > Don’t hold any capital > Investment Income is smaller > More frictional cost

TER = AMC + Fund Expense

True Return = Growth - Fund Expense
AB > BD > AD > BB


IE recognise profits earlier

Higher NBEV, recover strain

Deductions are charged based on fund value

If premium holiday, fund value is smaller than expected
Collect less fees
Similar logic to SC, costs early on are high, need to recover

Net asset growing due to sales
But cash balance rapidly dropping
Cash strain

Due to high FY bonus unit, comm etc


Insurers Prefer Unit-Linked Policies
	Commissions for these unit linked policies are the highest – which incentivizes intermediaries to focus on them more compared to traditional products
	These commissions are intentionally set by the company – this means that insurers are trying to sell more unit-linked products
	This is possibly due to the lower risk borne by the insurer (No guaranteed benefits) which would subsequently reduce the regulatory requirements on the insurer
	However, another view is that the product is much more complex and is harder to explain to clients which warrants a higher commission on the intermediary’s end
Excessive charges
	COnsidered investment securities and must be given a proespectus
Must be sold by registered individuals who pass a financial exam

BDAD BOP
BB AB EOP


Bid offer spread mechanicsd
Dividend take out rate

INV expense = Fund expense (lower than AMC) + OH
Fund manager gives rebate based on AUM/discsussion