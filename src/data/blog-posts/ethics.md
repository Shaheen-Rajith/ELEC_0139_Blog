---
title: Accountability, Bias, and the Ethics of AI in Healthcare
slug: ethics
publishDate: 08 May 2025
description: This post looks into the ethical risks of using AI in healthcare, from biased data and opaque decisions to accountability concerns.
---


The previous blog posts have shown the effect AI/ML can have on the healthcare domain but while these technologies offer unprecedented capabilities in treatment and diagnostics, they also raise serious ethical, legal and societal issues. Problems like bias, lack of accountability \& transparency, data privacy concern cause an overall lack of trust in such AI systems. In the UK, the National Health Service (NHS) has actively tried to integrate AI so as to increase efficiency and clinical outcomes. However, they have encountered multiple issues while doing so which will be described in more detail in this section of the blog as well as the risk if AI systems are left unchecked and what the UK and EU are doing to ensure that such technologies are used fairly and ethically.

## Bias & Fairness of AI in Healthcare

One of the main ethical issues in the usage of AI for healthcare is algorithmic bias. Bias happens when an AI model unintentionally favors some groups over others because of imbalances or flaws in the dataset used to train the ML models. In healthcare, such biases can even lead to clinical harm and erode people’s trust in the system. A recent example of this was pulse oximeters, which were found to overestimate blood oxygen levels in humans with darker skin tones. Although no AI was involved here, it highlights how even commonly used medical devices can have systemic flaws and biases [^pulseoxbias]. Imagine the outcome if similar issues happened in AI systems due to flaws in the data used. 

Studies have shown that ML models trained to detect melanoma performed much worse on test subjects with darker skin once again, it was attributed to the underrepresentation of such patients in the training dataset. ML models for chest X-rays and cardiovascular risk have also performed more poorly for minority classes like women and ethnic minorities. These cases are not coincidence, they are caused by using training datasets that disproportionately represent white, male, and affluent patients, this reinforces bias and inequalities in clinical outcomes. Also, when AI models are evaluated only on aggregate accuracy, their underperformance on smaller and underserved classes often goes unnoticed.

Bias can also arise from historical data that reflects disparities in procedure. Studies have shown that black patients in the UK have historically been prescribed less pain medication than white patients for the same conditions, due to racially biased assumptions about black people having a higher pain tolerance. If an AI system is trained on prescription records that reflect these disparities, it may think that certain ethnic groups need less pain medication. In practice, this could lead the model to recommend less aggressive pain treatment for black patients. 

<img src="/assets/blog/3_1.png" alt="SLUG" style="width: 55%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">Racial Bias in healthcare in the USA</p>
</div>


This creates a positive feedback loop where patients receive less care which is used to train the AI further resulting in future patients receiving even less care because the AI deems from the training data that they don't need as much medication. This is extremely dangerous and is effectively automated systemic discrimination [^ai_bias_healthcare]. Some methods can be used to reduce such bias resulting in more fair and equitable AI models such as:

- Diverse data sourcing to reflect real-world demographics
- Subgroup performance analysis instead of just overall accuracy
- Fairness-aware model selection, using metrics like equalized odds or demographic parity

A UK government review found that many medical devices, including AI ones show performance gaps across ethnic and gender lines. It recommended actions to consider fairness at every stage of the AI lifecycle from how data is collected to how systems are monitored after deployment [^equibias]. Bias in Healthcare is not just a matter of ethics, it is a clinical issue which if left unaddressed risks making existing inequalities even worse than it already is.


## The Need for Explainability and Trust

A major issue with many AI systems (especially complex deep learning models) is their lack of interpretability. In the case of healthcare, when workers aren’t able to interpret the working and understand how the AI model came up with the conclusion it reached. This opacity can cause serious problems, this is known as the Black Box Problem. There are tools for explaining how AI’s came to a decision like saliency maps and feature attribution methods which shows what part of an input influenced the models decision. But, these explanations are often misleading or unstable, highlighting areas that affect the output but don't mean anything clinically. This causes healthcare workers to not clearly trust the model’s reasoning. Research on trust in explainable AI (XAI) shows mixed results. When the explanations are clear and clinically relevant, they can improve confidence and lead to better diagnosing of patients, but when the explanations are vague/misleading, it can backfire, with workers relying overly on AI to the point that they trust the output, even when it’s wrong or not sensible [^explainability_medical_ai]. Development of Interpretable by design AI models can solve this issue, some methods they use are:

- Generalized additive models (GAMs), they weigh individual risk factors in a transparent manner to show how they come to some prediction
- Rule-based systems, they back up their predictions with if-then logic that healthcare workers can use to verify the results.

<img src="/assets/blog/3_3.png" alt="SLUG" style="width: 50%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;"></p>
</div>

<img src="/assets/blog/3_2.png" alt="SLUG" style="width: 50%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">Saliency Maps</p>
</div>

## Data Privacy, Consent, and Governance

Another major issue is the need of sensitive health data for training Healthcare AI models. Most developed countries have strict privacy regulations regarding medical data like electronic health records (EHRs), genomic data, and diagnostic image results. In the UK, there is the Data Protection Act 2018 which is aligned with the General Data Protection Regulation (GDPR)  [^dataprivacy]. AI research faces multiple real world barriers, Patient data is often siloed across multiple NHS trusts making it hard to train robust AI models using all the data. Even if the trusts collaborate, there are still complex approval processes and consent needed to gain access to the patient data. Deidentification techniques are usually used to anonymize the data but studies have shown that it is possible to reidentify over 80% of individuals in anonymized datasets using ML models trained on public data which is a huge privacy breach [^reidentification_risks]. Furthermore, some medical data like facial structure in cranial MRI’s are impossible to anonymize without losing out vital information. To mitigate these issues, the NHS have used the following privacy preserving methods:
- Federated Learning (FL), models are trained using decentralized data sources without actually moving the patient data off-site.
- Differential Privacy (DP), adds statistical noise to ML model outputs which prevents reverse engineering of individual records making it harder to reidentify individuals.
- Trusted Research Environments (TRE), are secure digital workspaces where researchers can analyze sensitive data without being able to download, copy, or misuse it thus minimizing the risk of data exposure [^tre].

<img src="/assets/blog/3_4.png" alt="SLUG" style="width: 50%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">Federated Learning</p>
</div>


## Legal Accountability and Shared Liability

As AI gets integrated into the medical field, it raises a lot of questions about accountability. If one of these models misdiagnoses a patient or outright suggests the wrong treatment plan, who is liable for it ? Is it the doctor who used the AI tool or the hospital, or the original developer that created said tool. Currently, the UK does not have any AI specific liability ruling, instead general medical rules can be applied. In this case:

- The healthcare worker can be held responsible for over relying on the AI tool
- The developer company can be held for creating software deemed defective.
- The hospital can be held responsible for failure in properly implementing the software without oversight.

But the question of Liability gets messy if we’re considering more complex AI systems with autonomy. There are AI systems that make decisions autonomously without any human override or transparency. If such systems misdiagnose, the responsibility will likely fall purely on the developers since the healthcare staff had no role in it. However, if AI systems are only used as a suggestion tool with the hospital staff having the final say in all decisions then the responsibility could be on the person who made the decision entirely [^legal_accountability]. The Medicines and Healthcare products Regulatory Agency (MHRA) maintains that AI tools are only to be used for assistance and that human staff should remain the final decision makers. However, as AI grows more complex, a more detailed framework is needed to determine responsibility in such cases.

<img src="/assets/blog/3_6.png" alt="SLUG" style="width: 70%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">More Examples of Liability</p>
</div>


## Regulation: UK and EU Approaches

Regulators in various countries are solving these ethical issues with different strategies. The EU’s AI Act, passed in 2023, is the world’s most comprehensive framework for high-risk AI applications such as those used in the healthcare domain [^eu_ai_act]. The EU AI Act contains sections on mandatory risk assessments, bias mitigation, requirements for human oversight and even mandates on transparency such as disclosing limitations. The UK meanwhile has opted for a more flexible approach to AI regulation. Instead of adopting a standalone AI bill, it has issued regulation white papers and asked existing bodies like the MHRA to adapt their ruling and to consider the role of AI [^uk_ai_regulation]. They have also introduced several practices to support safe and ethical AI such as:
- The AI Airlock Sandbox, which allows for real-world testing of new AI technologies in a safe environment
- Revised Good Machine Learning Practice (GMLP) guidelines
- Updated medical device classification rules to reflect the risks posed by AI
- Collaboration with international regulators like Health Canada to equalize AI safety standards

Ultimately, the goal is not just to build intelligent AI systems, we need to also ensure that the systems are operating justly and supporting healthcare delivery in a way that protects everyone including all minorities.

<img src="/assets/blog/3_5.png" alt="SLUG" style="width: 50%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">UK vs EU on AI Regulation</p>
</div>


<footer style="margin-top: 3rem; text-align: center;">
  <a href="/blog" style="padding: 0.6rem 1.2rem; background-color: #548e9b; color: #ffffff; font-size: 1.2 rem; border-radius: 25px; text-decoration: none; font-weight: 500;">
    ← Back to Blogs
  </a>
</footer>


---

[^equibias]: UK Department of Health and Social Care. *Independent Review on Equity in Medical Devices*, 2024. [Link](https://www.gov.uk/government/publications/independent-review-on-equity-in-medical-devices)

[^pulseoxbias]: UK Department of Health and Social Care. *Equity in Medical Devices: Independent Review*. 2024. [Link](https://assets.publishing.service.gov.uk/media/65e89f255b65240011f21b03/equity-in-medical-devices-independent-review-report-print-ready.pdf)

[^ai_bias_healthcare]: Carrie Stetler. *AI Algorithms Used in Healthcare Can Perpetuate Bias*. Rutgers University News. 2024. [Link](https://www.newark.rutgers.edu/news/ai-algorithms-used-healthcare-can-perpetuate-bias)

[^explainability_medical_ai]: E. Tjoa and C. Guan. *Explainability for artificial intelligence in healthcare*. BMC Medical Informatics and Decision Making, 2020. [Link](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-020-01332-6)

[^dataprivacy]: Information Commissioner's Office. *Guidance on AI and Data Protection*. 2023. [Link](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/guidance-on-ai-and-data-protection/about-this-guidance/)

[^reidentification_risks]: W.N. Price and I.G. Cohen. *Privacy and artificial intelligence: challenges for protecting health information in a new era*. BMC Medical Ethics, 2021. [Link](https://bmcmedethics.biomedcentral.com/articles/10.1186/s12910-021-00687-3)

[^federated_learning]: J. Xu et al. *Federated Learning in Healthcare: A Comprehensive Review*. IEEE Transactions on Biomedical Engineering, 2021. [Link](https://ieeexplore.ieee.org/document/9442683)

[^differential_privacy]: C. Dwork and A. Roth. *Differential Privacy in Health Data Sharing*. Annual Review of Statistics and Its Application, 2014. [Link](https://www.annualreviews.org/doi/10.1146/annurev-statistics-010814-020621)

[^tre]: UK Health Data Research Alliance. *Trusted Research Environments: A strategy to build public trust and meet changing health data science needs*. 2020. [Link](https://ukhealthdata.org/projects/aligning-approach-to-trusted-research-environments/)

[^legal_accountability]: J. Morley and L. Floridi. *Artificial intelligence in health care: accountability and safety*. Bulletin of the World Health Organization, 2020. [Link](https://www.who.int/bulletin/volumes/98/4/19-237543/en/)

[^eu_ai_act]: European Parliament. *EU AI Act: first regulation on artificial intelligence*. 2023. [Link](https://www.europarl.europa.eu/topics/en/article/20230601STO93804/eu-ai-act-first-regulation-on-artificial-intelligence)

[^uk_ai_regulation]: Medicines and Healthcare products Regulatory Agency. *MHRA's AI regulatory strategy ensures patient safety and industry innovation into 2030*. 2024. [Link](https://www.gov.uk/government/news/mhras-ai-regulatory-strategy-ensures-patient-safety-and-industry-innovation-into-2030)

