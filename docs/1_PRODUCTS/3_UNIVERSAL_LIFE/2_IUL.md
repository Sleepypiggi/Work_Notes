# **Indexed Universal Life**

**Indexed Universal Life** (IUL) is the a variant of UL where the crediting rate is **proportionate** to the return of a **specified index** (EG. S&P500):

* **Participation Rate** - Extent to which crediting rate follows the index return (%)
 
* **Cap Rate** - Maximum credited interest, after participation
 
* **Floor Rate** - Minimum credited interest, after participation

$$

$$

<—- Self Made —>
Insert picture

!!! Note

    The participation rate is typically non-guaranteed, but might have a minimum guaranteed level.
    
The expected crediting rate of IUL is **typically higher** than TUL due to the nature of underlying assets (Equity vs Bonds). All else equal, this also means that the **planned premium for IUL is lower**.

All other aspects of the product remain largely similar to a traditional UL.

## **Index Allocation**

Firstly, policyholders can choose to allocate their funds between:

* General Account (Same as UL)
* Index Account

!!! Note

    If premiums are allocated entirely to the general account, the policy effectively becomes a UL policy. In practice, insurers often require a minimum index allocation. 

The index account is then broken down into **multiple sub-accounts** depending on the policyholder’s chosen indices:

* Index Sub Account 1
* Index Sub Account 2
* Index Sub Account 3

!!! Note

    Most insurers typically provide a range of indices to choose from to suit the various risk profiles.
 
The crediting rate of each sub-account is based on the return of the corresponding index. In totality, the crediting rate on the entire index account is the **premium weighted average of the index returns**.

Operationally, **Segments** are created to track the amount of premium tracking a particular index during each crediting cycle (~annually).

Insert segment photo

For operational simplicity, segments are typically created on the same days each month. Before segments are created, the premiums are held in a **holding account**. Interest is also credited to the holding account, typically at an **identical rate to that of the general account**.

## **Index Return**

There are two commonly used methods to determine the index return:

* **Point-to-point** - Based on the return as at a specific start and end date (EG. 15 Jan 2026 to 15th Jan 2027)

* **Average** - Based on the average index return over a specified duration (EG. Daily Average, Monthly Average)
P

### **Hedging**

In order to provide the IUL payoff, the insurer **does NOT actually buy a mutual fund** that tracks the index. Due to the crediting floor, if the actual return of the fund drops below the floor rate, the insurer would **recognize the difference as a loss**.

Thus, the insurer instead uses **Options to hedge** the payoff, ensuring that that regardless of market movements, the desired crediting payoff is achieved:

* Buy ATM Call Option (Strike = Current Price)
* Sell OTM Call Option (Strike = Max Return)
* Combination is known as a Bull Call Spread

!!! Note

    When the Index Increases:
    
    1. Insurer will exercise their option to purchase at the initial level and sell at the current level
  
    2. Insurer is assigned to sell at the maximum level. If the market level is lower than the maximum, no assignment is made.
 
    3.  Insurer thus earns the net difference between the maximum price (or current price) and the initial price

<!—— Self Made —-> 

The cost of the purchased call will always be higher than the proceeds of the sold call, due to XXX. Thus, there will always be a **net cost** to build the hedge.

In order to fund the hedge, the insurer will invest the starting account value into a bond that matures at the next crediting cycle and use the return as their **Option Budget**:

* Bond - Provides the starting account value on maturity 
* Call Spread - Provides the credited interest on maturity




The leftover cash after the purchase of the bond together with the account charges are used to fund the purchase of the call spread. The excess can be recognized as profit for the insurer.

!!! Note

    Derivatives allow the insurer to leverage their position, allowing them to offer **participation rates higher than 100%** - simply by purchasing more calls.
    
    This allows IUL to have **minimum downside risk while having amplified upside risk**.
    
    Interestingly, this mechanism allows for indices with  relatively lower returns to still provide a high crediting rate.
   
### **Segmentation**

Interest is typically credited on a yearly basis. It is typical to use the point-to-point return of the index for a fixed day, but each insurer might have their own internal methodology.

For simplicity, policies that incept in the same month typically use the same reference day. Thus, a call spread will need to be **purchased each month** to generate the return.

Each tranche of options purchased each month is typically referred to as a Segment:

<—- Insert Image —>

Most modern IUL policies also have the option to spread the premiums across each month, achieving a **Dollar Cost Averaging** effect.

In this case, premiums are broken down into equal monthly amounts and are **invested into each monthly segment**, as opposed to entirely in one of the segments. The total interest credited will be the sum of the returns generated from the past 12 segments each policy anniversary.

!!! Note

    The relevant caps and floors will apply for each segment, not the 12 month rolling view.

### **Volatility Controlled Indexes**

Volatility Controlled Indexes (VCI) are synthetic indexes  that **automatically adjusts** the weight between an underlying specified index and a **low volatility asset class** (EG. Cash, Gold or Fixed Income) to achieve a target volatility level.

The primary purpose of VCIs are to lower the implied volatility of the underlying index, making the position **cheaper to hedge**.

The

### **Hedging Considerations**

Option Greeks



 





Distribution must be able to reach these ppl to sell

Bundled product means can only buy if u but others


From a projection perspective, for P/L Purposes, the Unit fund should have no surplus since it’s owned by the policyholder

Surrender Charge is also a deterrence against bank run

Need the funds to cover the future shortfall


Potentially higher costs - VUL policies may be more expensive than other types of permanent insurance, such as Whole Life 


lock your money up in all kinds of strange ways and do not compensate you for the illiquidity.


This makes a VL policy *potentially more attractive* than every other kind of policy. However, this is only true if the wreturn on investments outpace both inflation and the investment return of the insurer. Although equity does earn substantially higher returns over a *long* period of time, **short term deviations** are inevitable and the policy value could drop substantially if the investments go bad.



* **Variable UL**: Based on the performance of a specific mutual fund

Registered index universal life