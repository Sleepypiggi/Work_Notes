# **IFRS17 Overview**

## **Background**

IFRS stands for the **International Financial Reporting Standard**, which is a financial reporting framework to bring **transparency and consistency** to financial statements worldwide. IFRS17 is the set of standards that specifically cover the treatment of **insurance contracts**.

!!! Info

    There are two key IFRS standards for insurers:

    * **IFRS17** - Insurance Contracts (Liablities)
    * **IFRS9** - Financial Instruments (Assets)

    Both standards were designed to work in tandem with one another, thus they should be adopted together to prevent accounting mismatches between the two components.

It is important to have a clear **distinction** between the two common types of reporting:

* **Financial Reporting** - Provide **accurate and objective** information about the company in a **consistent** format to **external stakeholders** to facilitate their decision making.

* **Statutory Reporting** - Provide information about the company to **government authorities** to prove **compliance with relevant regulations**. Certain simplifications are allowed for operational ease. Given that Solvency is a primary concern, a more **conservative lens** is taken.

Another broad concept to understand is that IFRS17 is a **Principle Based** framework. It outlines the **intended outcomes** of the framework, giving insurers the **flexibility to choose the method** in which they achieve the outcome. As such, there are **no prescriptive methods or amounts** outlined as they view them as creating arbitrage opportunities.

## **Presentation**

IFRS17 adopts the view that an insurance should be treated as both a **Financial Instrument** and a **Service Contract**:

* If it were only treated as a financial instrument, it should be valued at its **fair value** (to be consistent with existing IFRS frameworks); the price it would go for if it would be sold in an orderly transaction. However, insurance contracts are **rarely traded**, making such approaches based on **hypothetical scenarios**.

* Instead, insurance contracts are typically **held till expiry**, where insurers provide the stipulated benefits over time as agreed. Thus, it is also treated as a **service contract**, which is valued based on the **insurance services provided** over time. 

Thus, the contract is typically split into two over-arching components:

* **Insurance Component** - Flows into **Insurance Service Results** in the P&L
* **Investment Component** - Flows into **Insurance Finance Income** in the P&L

<!-- From FRG Risk -->
![IFRS17_P&L](Assets/0_IFRS17_OVERVIEW.md/IFRS17_P&L.png){.center}

This split allows external stakeholders to **better understand the different aspects** of the insurer's performance.

## **Measurement**

### **Contractual Service Margin**

An insurance contract should be measured based on the **Fulfilment Cashflows** (FCF) of the contract, which incorporates the following components:

* Unbiased estimate of the future cashflows (neither conservative nor optimistic)
* Adjustment for the time value of money
* Adjustment for non-financial risk(s)
* Adjustment for financial risk(s)

The above can then be regrouped into three key components:

1. **Best Estimate Liability** (BEL) - Present value of the unbiased cashflows

2. **Risk Adjustment** (RA) - Present value of adjustment for non-financial (insurance) risks. It reflects the risk that actual experience might deviate from the best estimates.

3. **Time Value of Options & Guarantees** (TVOG) - Present value of the adjustment for financial risk. It reflects the risk that financial variables might cause embedded options and guarantees in the product becomes **in-the-money**.

!!! Warning

    Both BEL and TVOG are NOT officially defined terms under IFRS17; they were brought over from other valuation bases by the industry:

    * **BEL** - Officially defined under Solvency II
    * **TVOG** - Officially defined European and Market Consistent Embedded Values

!!! Warning

    Financial Risks are typically **accounted for implicitly** in the cashflows or discount rates. TVOG is typically the **only explicit adjustment**, hence it is emphasized above.

$$
    \text{FCF} = \text{BEL} + \text{RA} + \text{TVOG}
$$

On **Initial Measurement**, if the FCF is **negative**, the insurer expects a **net inflow**; the contract is expected to be **profitable**. In this case, the insurer will set up a positive **Contractual Service Margin** (CSM) under the LRC:

$$
    \text{LRC} = \text{FCF} + \text{CSM} = 0
$$

The CSM effectively represents the **excess of inflows over outflows** and is a measure of the **unearned profit** of the contract. It is set-up to ensure that the expected profit from the contract is **NOT recognized immediately**. This follows the principle of a **service**, where profit should be **recognized each period** based on the amount of service provided. Thus, the **CSM is amortized each period**, released as **revenue** under the insurance service results.

!!! Note

    IFRS17 uses the term *Measurement* when refering to the value of the contract. There are two key variations:

    * **Initial Measurement**: Contract valued **at policy inception**
    * **Subsequent Measurment**: Contract valued **post-inception**

On **Subsequent Measurement**, the following effects must be accounted for:

* **CSM accretes interest** based on the **initial discount rate**. This is to reflect the price of the service **at the time it is fulfilled** (time value effect). This is accounted for as an expense under investment results.

* CSM is adjusted for **changes in non-financial assumptions**. Given the inherent uncertain nature of the business, this is to reflect the insurers **latest expectation** of the business.

* Changes relating to **financial assumptions** (EG. Discount rate) are **NOT reflected in the CSM**. They will flow directly to the Insurance Finance Income line in the P&L.

!!! Note
    
    The CSM of a contract is essentially calculated using only the **discount rate at inception**, commonly referred to as the **Locked-In Rate** (LIR).

!!! Warning

    If subsequent measurement would cause the CSM balance to **become negative**, the CSM is instead **floored at 0** and any excess is set-up as a loss component instead.

    CSM is NOT allowed to be negative, except for reinsurance contracts held.

<!-- Obtained from IFRS Org -->
![CSM_ROLL_FORWARD](Assets/0_IFRS17_OVERVIEW.md/CSM_ROLL_FORWARD.png){.center}

Liability for remaining coverage
Liability for incurred claims

### **Loss Component**

If on initial measurement, the **FCF is positive**, then the insurer expects to **make a loss** on the contract instead. In this scenario, the insurer will instead set-up a **Loss Component** (LC) in the LRC instead. Similar to CSM, the loss component is **"amortized" (reversed)** such that the **LC becomes zero** by the end of the contract.

However, it is **IMMEDIATELY** recognized as an **expense** under the insurance service results. It is NOT a "negative CSM" that recognizes losses over time. This **asymmetric** treatment of profits and losses is a key concept in IFRS17.

Unlike CSM, the reversal of the LC has **NO impact on the total insurance service results**, but is needed to ensure that the revenue and expenses presented are sensible. Without the reversal, the amounts will be overstated.

* The reversal reduces BOTH the revenue and expense (neutral impact)
* IFRS17 states that the reversal must be done **systematically**, with relation to the expected claims, expenses & RA release (principle based)

<!-- Self Made -->
![LC_REVERSAL](Assets/0_IFRS17_OVERVIEW.md/LC_REVERSAL.png){.center}

### **Variations**

The measurement above are all based on the defualt measurement method, known as the **General Measurement Approach**. However, there are two other measurement methods that may be used, should certain conditions be met:

* **Variable Fee Approach**
* **Premium Allocation Approach**

### Aggregation

The fundamental principle of insurance is **risk pooling** - where the insurer issues a large number of **similar contracts**, where on average, the claims in any given period will be close to the expected value. Thus, contracts should be **measured in groups** to better reflect this.

However, since profit and losses are treated **asymetrically**, it is important **not to mix the two** together as there might be offsetting effects where **information is lost**:

* **Onerous** at recognition
* **Not onerous** at recognition and **no significant possibility** of becoming onerous
* **Others** - Not onerous but with possibility of becoming onerous

In totality, there are **three levels of aggregation**:

* **Portfolio** - Contracts with **similar risks** which are managed together (EG. Participating Whole Life, Universal Life)
* **Group** - Contracts with similar levels of profitability
* **Cohort** - Contracts **issued within one year** from one another, allowing **changes in profitability** of the business to be observed over time

!!! Warning

    Once the contracts are aggregated at initial recognition, **no changes** to the level of aggregation of the contract may be made - even if the contract subsequently changes profitability.

!!! Tip

    For new business, contracts will be **added to the cohort** until one year from the issuance of the first policy - at which the cohort becomes **closed**.

<!-- Self Made -->
![IFRS17_LOA](Assets/0_IFRS17_OVERVIEW.md/IFRS17_LOA.png){.center}



CSM measured at a group level
FCF can be at any level, typically most granular

## **Scope**

## Contract Boundary

Insurance contract definition >>
Contract is an agreement between two or more parties with enforceable rights and obligations

No longer required to provide coverage
No right to renewal

Discount rates

## **Reinsurance**

Accounted seperately
Because from a service stand point, RI does not reduce the amount it owes to the PH
It is that RCH is giving indemnity

RI premium
RI Ceding Commission  - Expense allowance for UW etc

RCH is usually an sset and paying toRI

Adjust for recits risk of the insurer

RI is an expense


## Revenue

Depicts revenue based on the amount service they expect to provide in the period

Investment Component
Amount that the entity is required to pay the policyholder even if the insured event does not occur
If investment component is interlinked with an insurance component, both under IFRS17 rather than splitting
Insurance component > additional amount that an entity would pay if an insured event occurs

Insurance finance expenses
Time value of money
Financial risk
Inflation

All in IFE or in OCI
