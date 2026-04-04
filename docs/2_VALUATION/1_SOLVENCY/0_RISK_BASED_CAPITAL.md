# **Risk Based Capital**

## **Background**

Given the **long-term** nature of life insurance where policy terms typically span over decades, the primary concern of policyholders is whether the insurer will still be operating at the time to make claim payments.

Thus, a large portion of life insurance regulations exist to **minimize the risk** of claim payment defaults. This is done via stringent **capital requirements** which requires the insurer to *minimally* maintain a prescribed level of assets over liabilities, which should provide an adequate buffer against unexpected claims.

Note that regulations CANNOT completely prevent the failure or default of an insurer without also hindering their operations, thus the regulation does not seek to fully prevent insolvency, but rather to ensure that the insurer can fulfil their **financial obligations** to policyholders.

## **History**

From the birth of insurance to the late 20th century, such regulations involved **FIXED capital requirements** that were arbitrarily based on the **judgment** of the regulators at the time. However, such regulations failed to properly account for the differences in risk across insurance companies as all companies had to hold the same amount, regardless of risk profile.

!!! Info

    For instance, regulators could mandate that all insurers had to at least hold **50 million** in assets at all times.

These regulations worked reasonably well till a large number of insolvency's in the late 20th century made it clear that it was **insufficient for modern life insurance** at the time. Thus, there was a push towards **Risk Based Capital** (RBC) requirements, where each insurer has a DIFFERENT capital requirement, **proportionate to their risk profile**.

## **Key Mechanics**

Most jurisdictions have adopted RBC requirements with slight variations. However, they all typically follow a similar structure where they require each insurer to determine a **Capital Ratio** of their available capital to their required capital (RC).

$$
    \text{Capital Ratio} = \frac{\text{Available Capital}}{\text{Required Capital}}
$$

The key mechanism is that there will be several **prescribed thresholds** that if breached, **grant the regulators authority** to take action against the insurer. There are typically at least two levels:

* **Higher Threshold**: If breached, insurer must submit action plan to restore capital
* **Lower Threshold**: If breached, regulator will be directly involved in the planning and/or implementation of above plan
* There could be **additional thresholds** which even allow the regulator to take control of the company or force the company to transfer its portfolio to another insurer

No matter how robust the framework is, **no single ratio** can give a complete picture of an insurers financial situation. However, it will allow the **early identification** of weakly capitalized insurers, allowing the corrective action to begin sooner, minimizing the chances of insolvency.

### **Required Capital**

The key idea of RBC is that insurers should hold capital proportional to the amount of risk they hold. The *minimum* amount of capital is known as the **Required Capital**. It typically has the following aspects:

* There are several **risk categories** (EG. Insurance Risk, Asset Risk)
* Within each category, it can be further broken into **sub-categories** (EG. Mortality Risk, Longevity Risk)
* RC for each sub-category is calculated as the **additional capital** needed to cover liability under that particular risk scenario
* The RC is **aggregated** within the sub-categories and then among the main categories to account for **Covariance** to reflect that these risks are **unlikely to occur together**

!!! Note

    For the calculation of sub-category RC under point 3, it is typically calculated as the **increase in liability** when the assumption relevant to the risk is **shocked**. For instance, the mortality risk could be calculated using **20% upward shock** to mortality. The amount to shock is typically prescribed by the local regulator, which is typically **calibrated** at a desired risk level.

    Most insurers are conservative and hold **more reserves** than the best-estimate liability. These prudence reserves can be used to contribute towards the required capital. However, since the conservatism assumed is typically **less than the prescribed shock**, insurers typically need to come up with **additional capital** to fulfil the required capital.

### **Available Capital**

The key idea is that not all items on the balance sheet will be **available to fulfil policyholder liabilities**. There are several key coinsiderations:

* **Capacity**: Is the asset available on a going-concern basis, during winding-up or both?
* **Subordination**: Does any other stakeholder have a priority claim to the assets?
* **Permanence**: Is the asset available perptually or does it have a maturity date?

!!! Note

    On the note of Permanence, an example of an asset with a maturity is a bond that was issued by the insurer to raise funds. The funds raised are available to the insurer, but only till maturity.

Most jurisdictions take the following approach to quantify available capital:

* Assets are split into different **tiers** and **sub-tiers**, based on the above considerations
* Restrictions are placed on the **proportion of capital** within each tier and between tiers
* Certain **regulatory adjustments** may be made to the amount of capital within each tier for other considerations
