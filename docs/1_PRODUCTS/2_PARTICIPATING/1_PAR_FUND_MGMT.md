# **Par Fund Management**

## **Overview**

Par fund management differs significantly from jurisdiction to jurisdiction depending on the level of regulation.

Par funds in Singapore are **highly regulated**, which requires a “Gated Par Fund” where par fund assets are **strictly ring fenced** from all other assets in the company.

In order to **safeguard policyholder’s interest**, shareholders **may NOT freely transfer any surplus** from the par fund to the shareholder owned funds to recognize as profit.

Whenever bonus is declared, insurers can also transfer a **maximum of 1/9** of that amount to the shareholder fund, known as a **Shareholder Transfer**. This effectively ensures there is **at least a 90:10 profit sharing ratio** between policyholders and the insurer.

Thus, the insurer is incentivized to declare as much as possible, with considerations for the sustainability of the fund.

## **Policyholder’s Reasonable Expectation**

Within the sales illustration, policyholders were shown an expected bonus that the company aims to declare. Despite disclaimers that the amount is non-guaranteed, policyholders typically **form an expectation** that this is the bonus they should expect to receive. This is known as **policyholder’s reasonable expectation** (PRE).

!!! Note

    There are many aspects other than the sales illustration which contribute to PRE - such as the general economic environment, practices by other companies etc.

Due to PRE, policyholders may feel cheated if the amount differs too much from what they expect. This has caused significant reputational issues in the past, thus insurers generally try to declare bonuses to meet PRE to avoid such issues.

This is accomplished by **Bonus Smoothing**, where surplus above the PRE is held back in “good” years to offset shortfalls in “bad” years, allowing them to consistently meet PRE. The fundamental assumption is that the economy moves in a cycle, thus the the market conditions **will eventually flip**.

However, there is a risk that the market stays down for a **prolonged period**, fully exhausting any previously accumulated buffer, creating the **risk of loss**. On the other extreme end, passing on the fluctuations each year may fail to meet PRE, but has **no risk of losses**.

Thus, bonus declaration methods typically sit somewhere in-between the two, depending on the company's risk appetite. It is very much **an art as it is a science**.

## **Asset Shares**

The par fund is typically managed in **tranches**, where similar policies are grouped together. This is typically done at the product group level, as these policies would have **similar levels of profitability**. Thus, the monitoring of surplus and declaration of bonus is done at this level as well.

!!! Note

    Policies could be grouped together in a variety of methods, typically by plan or inception year.

In order to determine the amount of available surplus, the amount of assets and liabilities are required of each block is required:

* Liability is typically **valued at the policy level**, thus the liability of a group of polices is simply the **sum of the liabilities** of each policy. This typically includes the **cost of guarantees** as well.
 
* Assets are held in **separate instruments** and are NOT directly attributable to specific policies. Thus, there is a need to **estimate each policies share** of the overall fund’s assets, known as the **Asset Share**.

<center>

|   **Policy Liability**   |       **Asset Share**       |
| :----------------------: | :-------------------------: |
|  Prospective Valuation   |   Retrospective Valuation   |
|   Estimate future cost   |  Estimate current position  |
| What insurer should hold | What insurer actually holds |

</center>

The asset share is effectively the **accumulated value** of the premiums received and any deductions (expenses, benefits etc) based on **actual experience** (financial and non-financial).

$$
\begin {aligned}
    \text{Asset Share}(t)
    &= (\text{Asset Share}(t-1) + \text{Premium}(t) -\text{Expenses} - \text{Benefits}) \cdot (1+i(t))
\end{aligned}
$$

!!! Note

    Asset Shares are a **general concept** that can be applied to any kind of policy. However, they are most used in a par context for bonus setting.

    It is possible to also use asset shares to estimate the profits made on a per policy basis by taking the difference between the asset shares and the payout of the policy.

Unfortunately, due to imperfections 

In an ideal world, the asset share will be exactly equal to the total assets in the par fund. However, due to imperfections in estimation or actual past operations, some discrepency is expected. It is typical that the actual policy assets is larger than the asset shares.



Asset Share is used to determine how much bonus to declare. Thus, some companies will gross up the Asset Share to the Estate amount, effectively zerozing the estate.





The payout on WP contracts is often the smoothed asset share. The terminal bonus is effectively the balancing item to achieve this.

Given that we are aiming to pay out approximately the asset share, we need to make sure that the regular bonuses aren’t too large, ie we don’t want the guarantees to be bigger than the asset share at maturity. One way to achieve this is to set regular bonuses equal to the bonus earning capacity (BEC). To calculate the BEC we project the asset share to maturity (today’s asset share plus premiums less cost of claims less expenses plus investment return) and equate it to the payout (current guarantees plus future regular bonuses plus an allowance for terminal bonus). The BEC is the rate of regular bonus that ensures equality betwee the projected asset share and the projected benefits.

This gross up/gross down amount is weighted based on the preliminary asset share calculated and distributed to each product. Then that is the final true asset share amount

## **Bonus Supportable Rates**


Par fund management

BSR = Bonus Supported Rate
Investment Return needed to support the current bonus assumptions

Compare against the current BEIR assumption to determine if the bonus rate is sustainable

Usually within some limit (+-1) of the BEIR is reasonable, no need to change

BSR is used to drive Bonus related decisions


Projecting the maximum illustrated assumed interest rates (generally, 12%), using current (or assumed) administrative expenses and current costs of insurance, without showing the prospective client several other assumed rates of return, creating a Blue Sky problem.

The divisible surplus will then be **split among all par policies** in an equitable way, depending on how much they contributed to the surplus. The mechanics of this split will be covered in the section on In Force Management.

Naturally, dividends are a **NGE** as they are dependent on the *past experience* of the insurer. Despite being non-guaranteed, insureds often feel cheated if what they receive is **significantly different** from what was advertised on the policy illustration. While the insurers were not at fault, this has caused reputational issues in the past thus it is in the insurers best interest to payout dividends at a rate **close to what was advertised**.

