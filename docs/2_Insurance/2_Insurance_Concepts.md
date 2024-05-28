# **Insurance Concepts**

## **How Insurance works**

### **Risk Pooling**

Insurers are willing to take on the risk of the insured because if they can take on the risk of other insureds, they can **pool the risks together**. This allows the financial loss (which would have been disastrous for a single insured) to be **spread among the group**, becoming manageable for all.

Consider a simple example to illustrate the concept:

1. There are 10 people inside the risk pool, each with a potential risk of $100.
2. We know for sure that 1 out of the 10 people will experience this $100 loss the next year.
3. If someone experiences a loss, then everyone within the pool will fork out $10 each.
4. This forms the $100 needed to cover the 1 unlucky person who experiences the $100 loss.
5. No matter whether an individual experiences the loss or not, they **only end up paying $10 to the pool**.

An insurance company helps to make the process **more efficient** by collecting the amount to be paid by each person beforehand (premiums) and then paying out the full amount to the unlucky individual shortly after the loss occurs. This also avoids the potential problem of someone not willing to pay their share.

This assumes that each risk in the pool **statistically independent** of one another, where it is *extremely unlikely* that a large portion of the insureds in the pool will make a claim at at the same time. This allows the insurer to collect a **fixed and relatively low premium** from every single insured and use them to pay only the small portion of insureds that makes a claim.

### **Law of Large Numbers**

Another key assumption of risk pooling is that the insurer knows the **Frequency** and **Severity** of the loss, thus knowing the risk of the insured.

$$
\displaylines{
    Risk = Frequency * Severity \\
    Expected~Loss = Probability~of~Loss * Amount~of~Loss
}
$$

Unlike determining the probability of a fair dice throw, there is no intuitive logic that can be used to derive these two values. Thus, the insurer needs to **estimate them from historical data** - from publicly available studies or their own studies on their insureds. These estimates are formally known as **Assumptions**. The actual values are known as the **Experience** of the insurer.

If the insurer has a sufficiently large pool of **statistically independent insureds**, then through the **Law of Large Numbers**, the estimated loss will be close to the actual loss of the group. This is because in a sufficiently large group, **on average**, the positive and negative deviations will offset one another, leaving the **estimate to be close to experience**.

Thus, the estimates can be used to *reasonably predict* the actual losses from the pool of poliyholders, allowing the insurance company to calculate an adequate premium to maintain the risk pool. In practice, most insurers also include premium provisions for other expenses and/or a profit margin.

<!-- Obtained from IAAAAI -->
![Law of Large Numbers](Assets/2.%20Insurance%20Concepts.md/LLN.png){: .center}

Through Risk Pooling and the Law of Large numbers, **unpredictable individual risk becomes predictable pooled risk**. This is identical to the concept of **Portfolio Diversification** in finance, where the **Non-Systematic Risks** (EG. An individual house catches fire) of the insureds are removed by pooling them together.

The insurer still faces some level of **Systematic Risk** that cannot be pooled away (EG. Asteroid hits earth and destroys all houses), but this is *significantly smaller* than any of the individual risks, which is why the insurer is willing to take on the risks of many.

### **Reserves**

The law of large numbers only guarantees that the derived probability will always be true **on average**, over multiple events. There could be times where the derived probability is different from the true probability, leading to **differences between the actual and expected losses** for the insurer.

Since the insurer collects premiums to cover for only the expected losses, a **larger than expected loss** in one particular year would mean that the insurer requires additional capital to pay off the claims. Thus, insurers are required to set aside a **Reserve** for their policies, where they can draw upon in times of larger than expected loss.

The reserve is meant to *supplement the collected premiums* in situations where the premiums were insufficient, to ensure that the insurer will be able to fulfil their claims, even in the unlikely event of larger than expected losses.

Insurers *simulate* these larger than expected losses by shocking the assumptions used. The shock is often referred to as a **Margin for Adverse Deviation** and is typically determined by the insurer.

| Low Margin | High Margin |
|:-:|:-:|
| Lower simulated loss | Higher simulated loss |
| Lower reserve held | Larger reserve held |
| Lower opportunity cost | Higher opportunity cost |
| May not be able to fulfil claims | Should be able to fulfil claims |

Each country has their own set of specific regulations on how the reserves should be calculated and how much capital must be actually held, which will be covered in their own respective sections.

## **Asymmetric Information**

The biggest problem in the insurance industry comes from **Asymmetric Information** - a situation where one party has more information than the other party, allowing one side to take advantage of it, to the other's detriment.

In insurance context, the two parties are the **Seller** (Insurance Company) and the **Buyer** (insured). Each side has little incentive to disclose any additional *negative* information that they have.

### **Buyer Ignorance**

The most understood form of asymmetry is known as **Buyer Ignorance**, where the **seller has more information** as compared to the buyer.

This is detrimental to the buyer as they end up buying a product that **appears good but is actually defective** (Lemon) in some manner that the seller was aware of, but not the buyer. This occurred because of the **Ignorance of the Buyer**, who was unable to identify the defects.

The average person would not be able to properly assess the value of an insurance policy or the financial health of the insurance company due to **complicated nature** of the product and the **inconsistent jargon** used across the industry. This could result in them purchasing less desirable policies that they otherwise would not have.

This is the reason why the insurance industry is **heavily regulated** across the globe - in order to level the playing field and combat buyer ignorance. For instance, regulators constantly monitor the financial health of insurance companies to ensure that they are solvent and require certain kinds of insurance to be purchased through a representative that will explain the terms of the contract.

### **Moral Hazard**

Moral Hazard refers to a situation where the **buyer has more information** as compared to the seller.

*After* being insured, insureds have an incentive to engage in **riskier behavior** relative to before they were insured. This is because sine they **do not have to bear the cost of the actions**, they become less careful and engage in riskier behaviour that they otherwise would not have before.

1. **Ex Ante** - Changes **Loss Prevention** behaviour; EG. Driving more recklessly, increasing the **Frequency** of accidents
2. **Ex Post** - Changes **Loss Minimization** behaviour; EG. Increasing the scope of car repairs, increasing the **Severity** of accidents

The effect is that this **increases the frequencies and/or severities of the losses** *after* the insurance contract has been made, which means that the premiums charged are *not sufficient* to cover the higher expected losses as a result of the moral hazard. This forces the insurer to **increase premiums** for all insureds to account for the increased losses due to the behaviour of a few.

There are four mechanisms to work around moral hazard, ensuring that there is **no incentive** to engage in riskier behaviour:

1. **Insurable Interest** -  The insured must have some *significant relation* to what is being insured. They should benefit MORE from the insured event NOT occuring rather than occurring.
2. **Indemnity** - Insurance should *compensate* for a loss, returning the insured back to their original position before the loss. The insured should not be left better off after an insurance claim
3. **Contribution** - If the insured owns *multiple policies*, then each policy will only compensate a portion of the amount, with the total equivalent to the loss. This is to ensure that the insured cannot seek compensation more than once; cannot be left better off after the insured event
4. **Subrogation** - If the insured experienced loss as a result of a third party, they forfeit the legal right to seek compensation from the third party. This is to ensure that the insured cannot seek compensation more than once; cannot be left better off after the insured event

Additionally, they could introduce an element of **responsibility** on the insureds end by introducing one or more **cost sharing mechanisms**:

1. **Co-payments** - A fixed amount that must be paid for by the insured
2. **Deductible** - A fixed amount of the *remaining* claim that must be paid for by the insured
3. **Co-insurance** - *Proportion* of the remaining claim that must be paid for by the insured
4. **Claim limits** - *Maximum* amount that the insurer will cover in a single claim or over a period; *excess* is paid for by the insured
5. Insureds typically have an option if they would like to have these cost sharing mechanisms in their policy. Naturally, policies with cost sharings have lower premiums than those without as they minimize moral hazard.

### **Adverse Selection**

Adverse Selection refers to a situation where the **buyer has more information** as compared to the seller.

Due to the nature of insurance, it often **attracts more high risk** insureds than low risk ones. This results in the risk pool being **systematically biased** towards high risk insureds, causing the average claims experience to be **higher** than that of a randomly selected group, to the insurers detriment as they are **not charging enough premiums**. Thus, there is a **natural selection of high risk insureds** to join the pool, leading to adverse outcomes for insurers.

This occurs because the insurer does not have enough information about the insured to distinguish between high and low risk ones. Thus, high risk insureds have an incentive to NOT disclose their additional information (to be charged lower), misrepresenting their risk profile.

This means that high risk and low risk insureds will be the paying the same premium. However, the higher risk individuals are **underpaying** relative to the risk they add to the pool while lower risk insureds are **overpaying** relative to the risk they add to the pool. The low risk insureds are essentially **subsidising** the higher risk ones, which is **unfair** to them.

This causes actual losses to be *consistently* larger than the expected loss (which they priced for), causing the insurer **lose money** over time. This would force the insurer to **increase premiums** to compensate for the loss, prompting *genuinely low risk insureds* to leave the pool as they will realise thay are overpaying for their insurance.

This further worsens the problem, as they recieve even lesser premiums than before, experiencing an even larger loss, increasing premiums once more. Eventually, the premiums are so high that **no one will be willing to buy insurance anymore**, causing the system to fail.

The most natural way to work around this is to **obtain more information** about the prospective insured to properly assess their risk. insureds will then be charged a premium **proportional to the level of risk** that they bring, overcoming the effects of adverse selection. This process is formally known as **Underwriting**, which will be covered in greater detail in the next section.

Alternatively, if it was **mandatory** to have the insurance, then low risk individuals cannot drop out of the pool, allowing the insurer to charge a higher premium without the system failing. A similar effect can also be achieved by offering **Group Insurance**, which typically consists of a good mix of high and low risk individuals.

Insurance paradox - if you want insurance, is damn suspicious
EG. Why you want? Is it you suddenly find out u got critical illness?

#### **Underwriting**

To underwrite a policy is to *guarantee* that the terms of the insurance policy will be upheld. This definition is similar to the finance definition, where the a financial institution underwrites a share issuance, *guaranteeing* that all shares will be sold (by purchasing unsold ones themselves).

In the insurance specific context, Underwriting is a **screening process** of determining the risk of a **prospective insured** and charging them a premium **proportional** to the determined level of risk, excluding them from certain coverage or refusing to underwrite the policy totally. Essentially, the insurer **price discriminates** insureds based on their level of risk, with the goal of **detecting and detering adverse selection**.

The screening process typically involves the requesting information relevant to the risk and their supporting documents. Insurance contracts are legally bound by the principle of **Utmost Good Faith**, which means that both parties must enter the contract in good faith - without the ill intention of deceiving the other. If it was found that the insured withheld material information (intentionally or not) from the insurer, the insurer thus has the **right to void the policy** and remove its obligation to pay out the claim.

Insurers then place the insured into one of various **Risk Classifications** that are based on Demographic Factors (Age, Gender, Smoking Status) or other relevant **Individual Factors**. Using these characteristics, insurers estimate the risk of a typical insured within the class. Using the estimates and the desired level of coverage, an appropriate level of premium is calculated.

In an ideal world, the insurer would like to precisely determine the risk of the insured. However, it is often hard to obtain the necessary information to do so because the insured would not disclose it, does not know about it or the necessary information simply does not exist. Thus, the risk classification provides an **as precise as possible** estimation of the risk, but it is not guaranteed to be perfect.

> For instance, smokers are statistically more vulnerable to developing certain types of Cancers. However, a particular smoker may have a genertic pre-disposition that prevents him from developing cancer. Since this information is usually inaccessible, the smoker will be charged according to the general trend.

Risk classifications are more accurate when there is **more data available about the risk**. As such, classifications for personal insurance tend to be extremely accurate as every individual experience similar risks. Conversely, commercial insurance classifications are not as accurate as the risks that each business faces is different from one another, thus cannot be used to accurately predict losses. Thus, commerical premiums may be significantly different from the risk classifications, as the underwriter may exercise their professional judgment to adjust the premiums based on their perceived risk of the insured (subject to various company level underwriting guidelines).

There is a **trade off** in Underwriting when it comes to high risk insureds. On one hand there is an inherent **desire to write more business**, which can be done by lowering premiums to incentivise them to take go forward with the insurance policy. On the other hand, a high risk insured below the required premiums adds **unnecessary risk** to the pool.

The tension between these two goals is especially strong because high risk does not necessarily translate to actual losses. However, insurance is one of the few industries where they can **earn more by selling less**, thus it is generally safer to write fewer risky accounts (earning less in premiums) than many risky accounts (earning more in premiums), as the long run claims typically have a greater impact than premiums.

## **How Insurance makes money**

### **Timing Problem**

Most traditional companies know the cost of their product before the sell it. For instance, a phone manufacturer knows exactly how much it costs to produce a phone, thus they know that the **difference in their price and cost** is the amount they will make or lose.

Insurance Financials
•	Insurance companies operate very differently from a traditional company - They collect Revenue (Premiums) BEFORE knowing the Cost (Claims) of their products
•	Since they may eventually have to pay out a claim, they cannot recognize these premiums as profits or freely use the capital they have gained
•	They have to hold enough liquid capital in order to pay off potential future claims. This amount is known as the Reserves, determined by the actuarial department
o
•	Companies can only recognize profit (Accounting sense) from insurance through a release of reserves. Reserves are typically conservative (Larger than what they expect to pay). Thus, if the actual experience reserves are lower than the reserve, the excess can be recognized as profit for the company
•	Standard accounting principles state that revenues and expenses must match the period in which they were recognised – but insurance is different. Thus, they have to follow a special set of accounting rules – IFRS17

How do Insurance Companies make money?
Investment Income
•	The main way they make money is through Investments. As stated earlier, there is a significant time gap between when premiums are paid and when a potential claim is made, if any at all. Insurers can invest the money during this time to generate revenue
o	Capital set aside as part of the reserves can only be invested in less risky assets such as Government Bonds or high-grade Corporate Bonds, which naturally yields a lower return
o	Remaining capital can be invested freely according to the insurer’s appetite in other asset classes as well (Equities etc)
o	Therefore, setting the reserves is so important – too high a reserve limits the investment capital while too low may put the company in financial distress
•	Therefore, insurance is known as a capital business – They obtain capital via Insurance Contracts for investments. Insurance contracts are a special form of Debt, thus this whole process of investment is akin to the concept of Financial Leverage
•	The competitive advantage of using insurance policies is that unlike regular debt, there is no fixed maturity date (if any at all) and no fixed redemption value (if any at all). But this is also the same reasons insurers are prone to financial distress
o	Thus, we can think of Insurance as a highly leveraged business
o	Berkshire Hathaway is a great example. Warren Buffet is known for his great investments, but not many realise that his investment capital comes from the insurance and reinsurance wing of Berkshire Hathaway
•	This is still a very high-level understanding of the process – it is actually a very complex process with only a few strategic personnel knowing how it works

Underwriting Profit
•	Another way that they can earn money is through Underwriting Profit – the difference between the premiums collected and what is paid out in claims and expenses
•	Most people believe that this is the main way that insurers make money given that this is what most consumers are exposed to. This idea is also perpetuated because of the misguided notion that insurers deny claims to increase profit
•	However, for many lines of insurance, the UW profit is often small, if not negative


## **Overview of Life Insurance**


1. **Death is inevitable** - Instead of focusing on *if* the policyholder will die, it is focused on **when** they will die
2. **Life is immeasurable** - Instead of indemnity, it provides a **pre-specified amount** chosen by the insured, known as the **Sum Assured (SA)**
3. **Insured is dead** - Instead of paying out to the insured, the payout is given to an **appointed individual**, known as the **Beneficiary**

Thus, Life Insurance is a contract where the Insurer pays the **Death Benefit** (Equal to the Sum Assured) to the appointed Beneficiary upon the death of the insured.