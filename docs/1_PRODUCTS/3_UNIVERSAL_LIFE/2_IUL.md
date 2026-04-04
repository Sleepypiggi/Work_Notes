# **Indexed Universal Life**

**Indexed Universal Life** (IUL) is the a variant of UL where the crediting rate is **proportionate** to the return of a **specified index** (EG. S&P500), subject to a minimum and maximum limit. IULs

All other aspects of the product remain largely similar to a traditional UL.



## 



Indexed Universal Life (IUL) is a variant of UL whose crediting rate follows the return of a specified underlying index (EG. S&P500). The extent to which the crediting rate follows the index is known as the **participation rate**.

Most insurers offer a range of possible indices, thus policyholders can typically allocate funds into one or more indices. In such cases, the credited interest will be the sum of the interest earned in each index sub account.

Apart from indices, allocation into the General Account (used for traditional UL policies) is also allowed. Thus, IULs can also be used to replicate a traditional UL policy by simply choosing to allocate 100% of the funds into the GA.

!!! Note

    IUL tends to be the most popular variation of UL as it tends to provide higher returns than traditional UL and less risk than variable UL.

### **Hedging**

The account of any UL policy is purely **notional**. The insurer does NOT actually purchase shares of the underlying index to support the policy. Recall that there is a crediting floor - if the insurer were to actually hold the assets and there was a loss, they would have to absorb the losses, exposing them to market volatility.

Thus, the insurer purchases an **At the Money Call Option** (strike = current market price) to produce the desired levels of return:

* **Index Increases**: Exercise option to purchase at the strike and sell at the higher market price
* **Index Decreases**: Do NOT exercise option

<!—— Self Made —-> 

However, notice that the option provides a payoff even beyond the crediting ceiling. Thus, in order to reduce the cost of the hedge, the insurer can sell a call option at the maximum crediting rate, creating a **Bull Call Spread** that provides a return **exactly between** the floor and ceiling:

<—— Self Made —->

If the index decreases, the account value remains the same. Thus, the insurer may **simply hold the account value in cash** to ensure that they at least have that amount. However, this method incurs an **opportunity cost** - thus, they instead **invest less than the full amount** into a short term bond such that the bond matures with approximately the original account value on the crediting date.

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
