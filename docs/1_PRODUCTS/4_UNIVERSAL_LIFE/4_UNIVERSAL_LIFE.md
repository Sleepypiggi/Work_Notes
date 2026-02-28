# **Universal Life Insurance**

## **Overview**

Universal Life Insurance is a plan where premiums are paid into a **notional account** that earns interest. The cost of insurance coverage (and other necessary expenses) are **deducted from the account** every period. The account value is also the **cash value** of the policy which can be **fully or PARTIALLY withdrawn** after an initial period. The policy lapses when the **account value is depleted**.

!!! Note

    It is possible that the interest earned on the account value exceeds the amount of charges, resulting in  a “self-sustaining” policy.

The interest earned on the account is known as the **Crediting Rate**, which typically has a **minimum floor** to ensure the account grows, but consequently also has a **maximum ceiling** on the returns. The insurer **earns the spread** of the crediting rate and their actual return on their investments.

Universal Life is known for its **flexibility** as the policyholder can choose **how much premium** to pay each period as well as **adjust their benefit** post-inception (subject to underwriting).

Given the above, the policyholder can effectively solve for the amount of premiums needed so that the resulting UL plan (assuming actual returns follow expected) **mimics another kind of policy** (Term, Endowment or WL).

!!! Tip

    It is useful to think of UL as a YRT with an account value, where the cost of the YRT is deducted from the fund.

### **Sum at Risk**

There are typically **two kinds** of Universal Life plans:

<center>

|      **Option A**      |       **Option B**       |
| :--------------------: | :----------------------: |
|  Level death benefit   | Increasing death benefit |
| Decreasing sum at risk |   Constant sum at risk   |

</center>

The policy will pay out either the death benefit or the account value. Thus, the cash value can be used to **fund the death benefit**. The shortfall is known as the **Sum at Risk** (SAR), which is the actual amount of coverage the insurer provides, which is the **basis for the COI** charge.

**Option A** universal life is a plan where the sum at risk changes based on the account value. In an ideal scenario where the account value is growing, option A results in a **decreasing SAR** over time. If the SAR reaches 0, then there is essentially NO insurance coverage provided, thus the policy is **no longer considered an insurance contract** and hence does not enjoy the typical statutory benefits.

Thus, to avoid the above scenario, the death benefit will be **automatically increased** once the account value catches up to it. The amount that the death benefit is increased is known as the **Corridoor**. It is defined as a **proportion** of the account value, typically the **minimum amount of SAR** that is needed to be considered an insurance contract.

**Option B** universal life is much simpler, where the death benefit is a combination of the account value and the sum assured. The death benefit scales proportionally with the account value, resulting in a **constant SAR**.

### **Planned Premium**

Since there are no premium requirements, policyholders have a high chance of under-paying the policy, causing it to **lapse earlier** than expected. Thus, the insurer usually recommends a premium amount that *SHOULD* keep the policy in-force to achieve a certain target (EG. Endow at age 100) based on their best estimate assumptions.

It is common to require the policyholder to pay at least the planned premium on inception.

However, there is **no guarantee** that the policy will achieve said target even if the planned premium is paid, as the actual crediting rate may be lower than assumed in certain years.

!!! Note

    In a universal life setting, to “Endow” means the account value grows to be equal to the sum assured.

!!! Warning

    UL is often marketed as a “whole life” product. However, this is misleading because there is no guarantee that the policy will remain in-force for life due to potentially lower than assumed crediting rates.
    
    This is contrary to other products where payment of the premium guarantees the coverage. Consumers who pay the planned premium consistently might see their policy lapse and “cheated” by the insurance company as a result.

### **Target & Excess Premium**

Since premiums are variable, so are the corresponding commissions. Thus, there is a risk that distributors might encourage policyholders to pay large amounts in order for them to earn higher commissions. To overcome this, premium paid **above the target premium** typically earns commission at a **reduced rate**.

Premium persistency rate

### **Crediting Rate**

Premiums are paid into the **General Account** of the policy and the crediting rate applied to this account is known as the **General Crediting Rate** (GCR).

The GCR is determined mainly based on the insurer’s investment performance over the period with some other consideration for smoothing and competitiveness.

!!! Note

    This is very similar to determining the Bonus for a Participating product.

In order to attract new business, insurers often offer a guaranteed crediting rate for a fixed duration, known as the **Ratelock Crediting Rate**.

Ratelocks are prospective. Thus, the rates offered are based on what assets are available to the insurer at the time of offering, with considerations for competitiveness as well.

Operationally, each policy will have two notional accounts:

* **General Account** - earns General Crediting Rate
* **Ratelock Account** - earns Ratelock Crediting Rate

If a Ratelock was offered at the time of inception, the **initial premiums** are allocated to the Ratelock Account. At the end of the Ratelock period, the amounts are re-allocated into the general account.

All subsequent premiums (regular premium or top-ups) are allocated into the General Account; or directly to begin with if there was no Ratelock offered.

<—- Insert self made diagram —>

### **Surrender Charge**

### **No Lapse Guarantee**

### **Premium Financing**

Premium financing is a method of purchasing a single premium insurance policy where a bank **loans a large proportion** of the required premium (typically 70-80%).


Use your own (non cash) assets as collateral for a bank loan for the premiums, allows you to purchase insurance while still staying invested in your business etc

Bank owns the policy? The cash value of the policy can be used as collateral as well, the difference between that and the loan amount is the collateral needed

UL is a high net worth focused product. Mainly comes in the form of SP policy

Supported heavily by premium financing - bank interest is 2%, UL credited rate is more than 2.0%

Policyholder essentially earn the spread

High net worth means branding is very important. Rich ppl want good service, good brand name, want to be able to tell ppl that they dropped X in this company etc.

How does it make sense that interest rate is 2 but credit 2.5?

If assets all in the same place, doesn’t make sense, high risk. If have global investment team, earned rate is higher than the borrowing cost

Also cos investment could be in non debt assets, earning higher rate than credited

Typically single premium
Pay loan interest every month >> still like a RP
gains realised only at the end

## **Indexed Universal Life**

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

HNW 1m
UHMW 30m
Self made professionals, entrepeneur or inherited
Business succession is the most important and longevity
High degree of personalization and established relationship
Typically single premium UL
White glove status > elite, solitaire 
Typically non taxable
Most important is the source of funds > Wher they get the money, is it money laundering or tax evasion
Single point of contact, active case management, tailored approach with value added services, confidentiality, coutesy calls, flexible access to advanced healthcare etc


Younger HMW > Aggressive wealth growth 
Older HWN > Conservarive wealth preservation 

Case size larger, underwriting more comprehensive