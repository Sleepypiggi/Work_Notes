# **Risk Based Capital** (RBC)

## **Background**

The primary objective of insurance regulators is to ensure that insurance companies can fulfil their financial obligations to policyholders. In other words, they want to ensure that insurers are **solvent**, having more assets than liabilities.    

This is done by imposing a **minimum amount of capital** that insurers must hold in order to run the business. Depending on the extent that insurers fall below this minimum threshold, the regulators have the legal authority to require submission of action plans to restore their capital position or to take control of the company. 

It is a common misconception to think that fulfilling the minimum capital requirements will ensure that solvency of the insurer. The purpose is for the regulators to monitor the performance of insurers and **identify weakly capitalized ones**, allowing them to take regulatory action to ensure that policyholders receive their promised benefits.

In the past, capital requirements were fixed; every insurer was subjected to the same amount. However, this failed to account for differences in the size and risk of the company, which led to many insolvencies in the US during the 1980s.

Thus, **risk based** capital requirements were created, where companies had different capital requirements **in proportion to their size and risk**.



## **Risk Based Capital 2 (RBC2)**

In Singapore, solvency is governed through the **Risk Based Capital 2** framework, outlined in [MAS Notice 133 - Valuation and Capital Framework for Insurers](https://www.mas.gov.sg/regulation/notices/notice-133).

## **1. Solvency Ratios**

Under RBC2, there are two key ratios that are measured - **Capital Adequacy Ratio** (CAR) and **Fund Solvency Ratio** (FSR).

Both have the same formula, but measured at different levels. CAR is measured at the company level while FSR is measured at the insurance fund level.

$$
\text{CAR/FSR} = \frac{\text{Financial Resources (FR)}}{\text{Total Risk Requirement (TRR)}}
$$

There are thresholds set by MAS for these two ratios:

* **Prescribed Capital Requirement** (PCR) - CAR/FSR > 100%
* **Minimum Capital Requirement** (MCR) - CAR/FSR > 50%

If the company does not meet the PCR, then they will need to submit an action plan to restore its capital position within a certain timeframe. If the company fails to meet to the MCR, then MAS has the right to revoke their license and impose management actions within the company.

In practice, MAS also sets another internal threshold above the PCR, usually around 135% for life insurers. Within the company, the threshold is usually higher, around 170%.

## **2. Financial Resources**

Tier 1 Resource
Tier 2 Resource
Concentration penalty

## **3. Risk Requirements**

Risk Requirements (or Risk Charges) are the minimum amount of *additional* capital (on top of BEL) that must be held by the insurer for taking on risk.

It is similar to PAD - it is additional capital that needs to be held to protect against unfavourable outcomes. However, there are two key differences. PAD only considers Insurance related risks and is internally set, while Risk Requirements also considers *non-insurance risk* and is *prescribed*.

The Total Risk Requirement is the sum of its **three components**:

1. C1 Risk Requirement - Insurance Risk
2. C2 Risk Requirement - Asset Risk
3. Operational Risk Requirement (ORR)

<!-- Obtained from Technical Specifications for RBC2 2018 -->
![Risk Requirement Diagram](RBC2%20Assets/Risk%20Requirements.png)

Note that TRR and each individual component is floored at 0 - it will *not* be negative. There will not be any reduction in required capital below BEL.

### **3.1 C1 Risk Requirement - Insurance Risk**

It is based on the risk associated with *insurance contracts* written by the company.

| Risk | Shock |
|:-:|:-:|
| Mortality Risk ||
| Longevity Risk ||
| Disability Risk ||
| Dread Disease Risk ||
| Expense Risk ||
| Lapse Risk ||
| Option Conversion Risk ||

It is unlikely that all these risks happen together at once - thus, there is no need to hold capital for ALL of the risks at once. We consider a **diversified risk requirement** instead - which will always be *smaller* than if the original values were added together.

The relationship between risks are prescribed in a correlation matrix:

<!-- Obtained from Technical Specifications for RBC2 2018 -->
![Risk Requirement Diagram](RBC2%20Assets/C1%20Correlation%20Matrix.png)

$$
\begin{align}
\text{Diversified C1} = \sqrt{Corr_{r,c} * C1_{r} * C1_{c}}
\end{align}
$$

#### **3.1a PAD vs C1**

C1 and PAD are very similar as both deal with Insurance Risk and involve shocking the assumptions used. The key difference lies in the assumptions shocked and the magnitude of the shock.

PAD = 90% Var ~ 50% of C1
C1 = 99.5
C1 Risk Charge = C1 Requiremtn - Pad

### **3.2 C2 Risk Charge - Asset Risk**

It is based on the risk associated with *assets held* by the company.

We can split the risk requirements into two categories - Market and non-market related risks. Similar to C1, we can consider a diversification between the two. The diversification factor is a fixed value of 0.5.

$$
\begin{align}
\text{Diversified C2} = C2_{misc} + \sqrt{C2^{2}_{Default} + C2^{2}_{Market} + 0.5 * C2_{Default} * C2_{Default}}
\end{align}
$$

Within the market risks, we can also consider a diversification benefit between them. There is a different correlation matrix to use, depending on which interest rate scenario is used.

$$
\begin{align}
C2_{Market} = \sqrt{Corr_{r,c} * C2_{Market,r} * C2_{Market,c}}
\end{align}
$$

<!-- Obtained from Technical Specifications for RBC2 2018 -->
![C2 Correlation Matrix](RBC2%20Assets/C2%20Correlation%20Matrix.png)

### **3.3 Operational Risk Requirement**

Operational risk refers to the risk of loss arising from company operations such as inadequate internal controls or processes, organisational changes or human errors.

It is harder to monitor every process within a larger organization, thus the operational risk requirement is calculated based off the size of the firm, measured through either premiums or liabilities of the firm.

$
\\ORR_{Premium} = 4\% * GWP_1 + max(0, 4\% * (GWP_0 - GGP_1) - 20\% * GWP_0)
\\ORR_{Liabilities} = 0.5\% * \text{Gross Liabilities}
\\ORR_{Calculated} = Max (ORR_{Premium}, ORR_{Liabilities})
$

GWP stands for Gross Weighted Premium, which is measure of the premium received during a specified period. It is used to account for fluctuations in Single and Limited Pay business, which tends to be sensitive to market conditions.

| Premium Paying Term | Weight |
|:-:|:-:|
| Single Pay | 10% |
| Limited Pay | 10% * Number of Years |
| Regular Pay | 100% |

### **3.4 Total Risk Requirement**

Similar to before, it is unlikely that both C1 and C2 risks occur together, thus we consider a diversified risk requirement instead.

$$
\text{Diversified C1 and C2} = \sqrt{C1^{2} + C2^{2}}
$$

Similarly, the operational risk requirement should not take up a significant portion (~10%) of the overall requirement.

$$
\text{ORR} = Min(ORR_{Calculated}, 10\% * (\text{Diversified C1 and C2}))
$$

Thus, the total Risk Requirement is the sum of all three final components:

$$
\text{TRR} = (\text{Diversified C1 and C2}) + \text{ORR}
$$

## **4. Discount Rates**

As with Valuation, Risk Requirements are calculated using risk free rates obtained from government yield curves.

Insurance cashflows are extremely long term, thus requiring a risk free rate spanning up to a maximum of 100 years. However, governments typically do not issue such super long lasting bonds.

The longest bond issued is around 20 to 30 years long. Even if there was a bond that lasted up to 100 years, it will probably be a rare one-off exception. Thus, there is insufficient liquid data to determine the risk free rate beyond the 20-30 year time horizon.

### **4.1 Smith Wilson Method**

The smith-wilson method can thus be used to extrapolate the risk free rate beyond the 20-30 year horizon up till whatever time horizon required.

It is based off three key concepts:

1. **Last Liquid Point** (LLP) - the last period at which liquid government yield curve data is available
2. **Ultimate Forward Rate** (UFR) - a proxy for the long term economic interest rates
3. **Convergence Point** - the first period at which the UFR starts

The idea is to split the time horizon into three distinct segments:

| Time Horizon | Spot Discount Rates |
|:-:|:-:|
| Valuation Date to LLP | Government Yield Curve data |
| LLP to Convergence Point | Extrapolate from LLP to UFR |
| Convergence Point Onwards | Derived based on UFR |

<!-- Obtained from Technical Specifications for RBC2 2018 -->
![Smith Wilson Method](RBC2%20Assets/Smith%20Wilson.png)

MAS has prescribed the LLP, Convergence Point and UFR to use for most major currencies:

<!-- Obtained from Technical Specifications for RBC2 2018 -->
![Other Currency Parameters for SW Method](RBC2%20Assets/SW%20Other%20Currencies.png)

The only parameter that is not prescribed is the **Speed of Convergence** $\alpha$, which controls the rate at which the LLP moves towards the UFR. It is to be chosen in such a way that results in an acceptable level of divergence from the UFR at the convergence point.

### **4.2 Matching Adjustment & Ill-liquidity Premium**

Discounting
Matching Adjustments
If Assets and Liabilities are met, then it means that the assets held are long term
Should have higher yield, can increase discount rate and hence decrease PV of liabilities

Ill Liquidity premium
Long term assets are ill liquid (hard to sell) thus should get higher return than RFR
can increase discount rate and hence decrease the PV of liabilities

and at the fund/asset level > Because all liabilities are backed by funds (Balance sheet concept)

Insurance funds > Overseas Insurance Funds (OIF) vs Singapore Insurance Funds (SIF)
Policy type > Par vs non par

Asset = Liabilities

Current liabilities
Surplus

ILP/Non par = RFR
PAR = ASSET + INv yield

The Smith-Wilson method is part of the broader class of curve-fitting techniques. It is designed to fit a term structure of interest rates to observed market data, such as swap rates or government bond yields, and then extrapolate that term structure to longer maturities where market data may be sparse or unavailable

The method starts by fitting the term structure to the observed market rates. It ensures that the term structure reproduces these rates accurately at the given maturities.

For maturities beyond the available market data, the Smith-Wilson method extrapolates the term structure towards an ultimate forward rate (UFR). The UFR reflects the long-term equilibrium interest rate that the market expects.

The extrapolated rates smoothly converge to the UFR as the maturity increases, ensuring a realistic and stable long-term projection.
The extrapolation aligns with the prescribed UFR by the MAS, which reflects a long-term stable interest rate.

This approach under RBC 2 helps ensure that the valuation of liabilities is robust and reflective of both current and expected future market conditions, thus contributing to the overall financial stability of the insurance sector.

Always converge to UFR; LT spot rate is always the same

The UFR represents the long-term equilibrium interest rate towards which the extrapolated yield curve is expected to converge. It reflects the long-term expectations of interest rates based on macroeconomic factors.

Purpose: The parameter α (often referred to as the convergence speed or decay factor) controls the speed at which the yield curve converges to the UFR.
Effect: A higher α value results in a faster convergence of the yield curve towards the UFR, while a lower α value means slower convergence.

A high Alpha value will make the yield curve steep at shorter maturities, moving quickly towards the UFR, while a low Alpha value leads to a flatter curve, with the long end of the curve approaching the UFR more gradually.

Exponential Decay: Alpha is associated with the exponential decay function in the Smith-Wilson framework. The function typically looks like e−αte−αt, where tt is time (or maturity). This decay function influences how much weight the extrapolated curve gives to the UFR as opposed to observed market data.

The Matching Adjustment is intended to reduce the artificial volatility in an insurer’s balance sheet by recognizing the additional return that can be earned from holding illiquid assets over long periods, where the insurer's liabilities are also illiquid.

It provides a way to reflect the insurer's ability to hold assets to maturity, thereby allowing the valuation of liabilities to more closely align with the expected returns on the corresponding assets.

To apply the Matching Adjustment, the insurer must demonstrate that the assets are closely matched to the liabilities in terms of both timing and amount. The cash flows from the assets must closely match the expected cash flows from the insurance liabilities.

The Matching Adjustment is calculated as the difference between the yield on the matching assets and a risk-free rate, adjusted for the cost of credit risk (often referred to as the Fundamental Spread).

By using the Matching Adjustment, insurers can reduce the present value of their long-term liabilities, which in turn can reduce their capital requirements under the RBC 2 framework. This reflects the lower risk associated with holding matched assets and liabilities.