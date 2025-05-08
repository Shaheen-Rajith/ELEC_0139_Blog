---
title: Accountability, Bias, and the Ethics of AI in Healthcare
slug: ethics
publishDate: 08 May 2025
description: This post looks into the ethical risks of using AI in healthcare, from biased data and opaque decisions to accountability concerns.
---


The previous blog posts have shown the effect AI/ML can have on the healthcare domain but while these technologies offer unprecedented capabilities in treatment and diagnostics, they also raise serious ethical, legal and societal issues. Problems like bias, lack of accountability \& transparency, data privacy concern cause an overall lack of trust in such AI systems. In the UK, the National Health Service (NHS) has actively tried to integrate AI so as to increase efficiency and clinical outcomes. However, they have encountered multiple issues while doing so which will be described in more detail in this section of the blog as well as the risk if AI systems are left unchecked and what the UK and EU are doing to ensure that such technologies are used fairly and ethically.

## Bias & Fairness of AI in Healthcare

One of the main ethical issues in the usage of AI for healthcare is algorithmic bias. Bias happens when an AI model unintentionally favors some groups over others because of imbalances or flaws in the dataset used to train the ML models. In healthcare, such biases can even lead to clinical harm and erode people’s trust in the system. A recent example of this was pulse oximeters, which were found to overestimate blood oxygen levels in humans with darker skin tones. Although no AI was involved here, it highlights how even commonly used medical devices can have systemic flaws and biases. Imagine the outcome if similar issues happened in AI systems due to flaws in the data used. Studies have shown that ML models trained to detect melanoma performed much worse on test subjects with darker skin once again, it was attributed to the underrepresentation of such patients in the training dataset. ML models for chest X-rays and cardiovascular risk have also performed more poorly for minority classes like women and ethnic minorities. These cases are not coincidence, they are caused by using training datasets that disproportionately represent white, male, and affluent patients, this reinforces bias and inequalities in clinical outcomes. Also, when AI models are evaluated only on aggregate accuracy, their underperformance on smaller and underserved classes often goes unnoticed.

Bias can also arise from historical data that reflects disparities in procedure. Studies have shown that black patients in the UK have historically been prescribed less pain medication than white patients for the same conditions, due to racially biased assumptions about black people having a higher pain tolerance. If an AI system is trained on prescription records that reflect these disparities, it may think that certain ethnic groups need less pain medication. In practice, this could lead the model to recommend less aggressive pain treatment for black patients. This creates a dangerous feedback loop where over time future patients receive suboptimal care depending on race. Such models are basically an automated form of systemic discrimination, making disparities even worse instead of solving them. To address this issue, people are calling for an equitable design approach that includes:
- Diverse data sourcing to reflect real-world demographics
- Subgroup performance analysis, not just overall accuracy
- Fairness-aware model selection, using metrics like equalized odds or demographic parity


A UK government review found that many medical devices, including those using AI, show performance gaps across ethnic and gender lines. It had recommended actions to embed fairness at every stage of the AI lifecycle from how data is collected to how systems are monitored after deployment [^equibias]. Bias in Healthcare is not just a matter of ethics, it is a clinical issue which if left unaddressed risks making existing inequalities even worse than it already is.

## The Need for Trust & Explainability


<img src="/assets/blog/Fig-2.png" alt="SLUG" style="width: 30%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">Caption</p>
</div>

HIQEBIWHFBWHFBLIHEFBWHFBOHFB IWEBHFIWB IWHBFWOFHBWOEFY@O iqeHDOIEBO OYGOFYGO*GD*YEGD@O*)E&DFG)&$DGP@&GDOLYEDGBULOGUGY

<footer style="margin-top: 3rem; text-align: center;">
  <a href="/blog" style="padding: 0.6rem 1.2rem; background-color: #548e9b; color: #ffffff; font-size: 1.2 rem; border-radius: 25px; text-decoration: none; font-weight: 500;">
    ← Back to Blogs
  </a>
</footer>


---

[^equibias]: UK Department of Health and Social Care. *Independent Review on Equity in Medical Devices*, 2024. [Link](https://www.gov.uk/government/publications/independent-review-on-equity-in-medical-devices)
