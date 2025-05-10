---
title: How AI is Actually Changing Healthcare
slug: main
publishDate: 05 May 2025
description: This post describes how AI is actually being used in healthcare, with applications in medical imaging, diagnostics, and decision-making.
---

While the previous blog post talked about the current state of the healthcare domain and made the case for adopting AI/ML tools, it’s just as important to understand the actual technology behind it and look beyond just the hype. Different tools solve different problems, from reading scans to predicting diseases. This post explores five key AI/ML tools, how they work and how they are already making a difference and solving challenges in the sector. 

## Computer Vision

Computer Vision is the sub-branch of AI that deals with computers being able to analyse images and it is revolutionizing medical imaging. Instead of just analyzing singular pixels as is done in a basic neural network (ANN), computer vision models are able to recognize patterns and features like shadowy nodules in the lungs which could be a sign of cancer, just like an experienced radiologist can. These models are experts at detecting subtle patterns that even most humans might overlook and are both consistent and fast at it. They typically use Convolutional Neural Networks (CNN) [^techradar2025] which uses multiple filters in 2D-Conv layers where the filters are passed over the input image to detect patterns like edges or shapes. Early layers might pick up simple features while the later layers use that information to capture more complex features like tumors in lung scans. These filter values get fine tuned during the training stage while thousands of labeled images are used to get the model to learn and identify relevant features in them. Such CNN based tools can act as a second pair of eyes passing on any information they get to the healthcare staff.

<img src="/assets/blog/2_1.png" alt="SLUG" style="width: 60%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">CNN Architecture</p>
</div>

Computer vision is tackling numerous healthcare challenges, it can identify abnormalities in radiology images like CT scans, MRIs, and X-rays or assist in pathology by scanning slides for cancer cells. In eye care, AI systems can be used to analyze retinal scans and check for diabetic retinopathy early. In dermatology, they can check photos of skin lesions for melanoma risk. The main goal is to reduce the heavy workload of specialists and improve accuracy as well. As seen in the previous section, AI tools have been able to outperform even expert radiologists when it comes to  tasks like detecting pneumonia from chest X-rays or even identifying early signs of cardiovascular disease. Health centres can also integrate AI tools to prioritize urgent cases so that patients who need urgent care from specialists can get it in time.

The NHS has already started deploying such tools at scale. In 2023, NHS England created an AI Diagnostic Fund to adopt approved AI models. An AI system by Annalise.ai that can detect 124 different findings on chest X-rays from lung nodules to misplaced medical tubes is being rolled out to over 40 NHS trusts [^annalise2024]. At NHS Grampian in Scotland, UK where it was tested; the AI cut the time from X-ray to lung cancer treatment by an average of 9 days. Such gains can be life-saving, given how important starting treatment early is for diseases like cancer. Another example is breast cancer screening where in a 2023 NHS trial of 10,000 mammograms [^guardian2025],  An AI system developed by  Kheiron Medical found early signs of breast cancer in 11 women that human doctors had missed. These cancers were near impossible to detect using the human eye yet the AI was able to do it. The goal is that by integrating computer vision models into screening programs, cancers and other diseases can be caught at an earlier stage [^sciencedirect2024]. In all these cases, the AI only suggests its prediction but the final decision is made by the healthcare workers which makes Liability interesting if something goes wrong, more about this will be explained in the next section. When used responsibly, computer vision in healthcare is a powerful helper, reducing workloads and potentially saving lives too.


## Natural Language Processing (NLP)

NLP is the sub branch of AI that allows computers to understand human language and emotions/meanings from text. They use models like Transformers (which is what is used in LLMs like ChatGPT) to parse through the given text [^turn0search0]. A large amount of medical information exists in text form such as doctors prescriptions, nurses reports or lab test data. NLP models can read them and extract useful information from it or even generate new text from it. By training these models on a vast amount of medical data, they are able to learn medical terminology and understand all the abbreviations and complex terms. It can even capture context from sentences so for example if a sentence contains “Jaguar”, the program can understand if it's talking about the animal or car company. NLP can drastically reduce burdens on administrative tasks by automating them, they can be used to listen to conversations with patients and generate notes or letters as needed. It can be used to parse through patient records and extract any useful information from them instead of having staff manually go through each record. NLP can power chatbots which can answer patient questions and have full conversations with them, or even help them book appointments [^turn0search2].

<img src="/assets/blog/2_2.png" alt="SLUG" style="width: 70%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">NLP Pipeline for processing Health Records</p>
</div>

The NHS has also  trialed NLP models such as an AI assistant called TORTUS. In 2024, Great Ormond Street Hospital led a London-wide pilot with 5,000 patients to test whether an NLP system could streamline documentation [^turn0search1]. The TORTUS system uses speech recognition and a generative AI backend to listen to clinical consultations and draft the outpatient letters and notes automatically. Doctors would then review and edit the drafts before finalizing the document. The main aim was to reduce time doctors spent in front of the computer screen and let them focus more on patients. Early results were positive and doctors reported that it can significantly reduce time spent on writing letters, potentially increasing face-to-face time with patients. Dr. Dominic Pimenta, TORTUS’s developer, noted that this kind of AI tech could “massively improve healthcare workers’ lives” and relieve pressures if proven safe and effective.

<img src="/assets/blog/2_tot.png" alt="SLUG" style="width: 70%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">NLP Pipeline for processing Health Records</p>
</div>

Beyond documentation, NLP is also helping make medical information more accessible. Researchers have explored using large language models like GPT-4 to simplify medical jargon in clinic letters into plain English for patients. This could bridge communication gaps, ensuring patients understand their care better. Moreover, chatbot-based symptom checkers which some NHS services have already experimented with in triage settings use NLP to interpret a patient’s text descriptions of symptoms and asks follow up questions, mimicking a nurse’s triage process [^turn0search3]. While such chatbots must be used cautiously, they show how conversational AI can improve healthcare. The key with NLP in healthcare is maintaining accuracy and empathy as the AI must not misinterpret critical details or generate incorrect info which could lead to disastrous consequences.


## Generative AI

This is the sub branch of AI that consists of models that create new data such as images, text or time series data by learning patterns in the existing training datasets. Instead of just analysing the training data, they try to generate synthetic data that resembles it. Some common types of models used for this are Generative Adversarial Networks (GANs), Variational AutoEncoders (VAEs) and Large Language Models (LLMs) [^topol2024]. GANs consist of two parts, the generator and the discriminator. The generator produces synthetic data while the discriminator tries to check if the data is real or fake (synthetic). Through training, the generator gets better at producing data close to the real training samples. CycleGAN is a special type of GAN that actually contains two GANs which work in tandem. This setup allows it to be used for tasks like image translation from one domain to another like converting MRI scan images to CT scan images, and this can be done without needing paired training data.

<img src="/assets/blog/2_3.png" alt="SLUG" style="width: 70%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">CycleGAN Architecture for Image Domain Translation</p>
</div>

With reference to the healthcare domain, generative AI is currently being used in imaging, documentation, simulation and even drug discovery. In medical imaging, generative AI models are used to augment existing dataset, to add synthetic data for minority classes. They can be used to create synthetic patient health records to safely train and test ML models with any worry about breaching privacy. LLMs can be used to help workers in drafting sick notes or other required documents like discharge summaries. In the pharmaceutical sector, which is related to healthcare, generative models are able to generate novel molecules for drug research. Hospitals are even testing the concept of “digital twins” which are virtual patient simulations to test treatments from actually applying them to the real patient [^mathews2024]. A real world example of Generative AI in healthcare is seen in the research paper that managed to train a CycleGAN to convert between MRI and CT style brain scan images [^CGAN]. Since MRIs show soft tissue well while CTs show bones well, doing both tests is the ideal choice, but patients are often not able to get both due to a multitude of reasons. The AI was trained on unpaired public datasets and learned to generate CT-like images from MRIs. This helped radiologists visualize bone structures without extra tests or radiation exposure. This has high potential in brain tumor analysis and radiotherapy planning. Also, as mentioned above, the TORTUS project in the UK trialed NLP models  along with a generative AI backend to automatically draft outpatient letters, cutting documentation time. Such synthetic data must always be validated before use as these outputs are worthless if they are medically inaccurate, Generative AI models like LLMs are also prone to Hallucination where they output clearly wrong facts and thus proper regulations must be in place, more about this will be discussed in the next section.


## Remote Monitoring + ML

Wearable as well as remote health monitoring tools are changing how healthcare is considered outside hospitals and clinics. Devices like smartwatches and fitness trackers can track various vital signs like heart rate, blood oxygen, breathing rate, amount of activity and so on continuously [^mayo2024]. ML tools can be used to extract information from this data, spotting subtle changes in the vital signs that indicate worsening health. Predictive analytics can also be done when the live data is used along with historical data to spot health issues before they become noticeable normally or before it becomes life threatening. Various kinds of ML models can be used for such tasks like basic decision trees, or neural networks or more commonly an ensemble method. Such models allow people to start treatment early instead of waiting for symptoms and then getting it diagnosed. Such Smart devices can even flag more serious diseases like abnormal heart beats or lung issues. Hospitals can even use such tools to track which patients are more likely to end up at the hospital again. The NHS had trialed an app based system called ACE-CF which monitors cystic fibrosis patients [^acecf2024]. By analysing lung data, the system can flag the possibility of infections upto 10 days earlier. 

<img src="/assets/blog/2_4.png" alt="SLUG" style="width: 25%;">
<div class="img-caption">
  <p style="font-size: 0.9em; color: #555; text-align: center;">ACE-CF App Dashboard</p>
</div>


Another project by Cera looks at home visit records to flag fall risks for older people [^cera2024].  The NHS claims that these projects help cut down thousands of avoidable hospital visits daily. UCL , along with King’s College London are working with NHS England on a national project called foresight which uses generative AI to make predictions about patients on things like hospitalizations and diagnoses [^uclforesight2024]; it is trained using over 50 Million anonymized records. Such systems are obviously not perfect and the predictions can often reflect bias in the training data. The next post will cover the Ethical side of using AI for healthcare in more detail.



<footer style="margin-top: 3rem; text-align: center;">
  <a href="/blog" style="padding: 0.6rem 1.2rem; background-color: #548e9b; color: #ffffff; font-size: 1.2 rem; border-radius: 25px; text-decoration: none; font-weight: 500;">
    ← Back to Blogs
  </a>
</footer>


---

[^annalise2024]: Annalise.ai. *Transformational AI diagnostic tool made available to radiologists in over 40 NHS trusts*. 2024. [Link](https://annalise.ai/2024/06/transformational-ai-diagnostic-tool-made-available-to-radiologists-in-over-40-nhs-trusts/)

[^guardian2025]: The Guardian. *NHS to launch world's biggest trial of AI breast cancer diagnosis*. 2025. [Link](https://www.theguardian.com/society/2025/feb/04/nhs-to-launch-worlds-biggest-trial-of-ai-breast-cancer-diagnosis)

[^sciencedirect2024]: ScienceDirect. *Early cancer detection using deep learning and medical imaging*. 2024. [Link](https://www.sciencedirect.com/science/article/pii/S1040842824002713)

[^techradar2025]: TechRadar. *What are convolutional neural networks?* 2025. [Link](https://www.techradar.com/pro/what-are-convolutional-neural-networks)

[^turn0search0]: Aadit Jerfy. *The Growing Impact of Natural Language Processing in Healthcare*. *National Center for Biotechnology Information*, 2024. [Link](https://pmc.ncbi.nlm.nih.gov/articles/PMC11475376/)

[^turn0search1]: Great Ormond Street Hospital. *GOSH pilots AI tool to give clinicians more quality-time with patients*. 2024. [Link](https://www.gosh.nhs.uk/news/gosh-pilots-ai-tool-to-give-clinicians-more-quality-time-with-patients/)

[^turn0search2]: Simon Cork. *Evaluating ChatGPT for converting clinic letters into patient-friendly language*. *BJGP Open*, 2025. [Link](https://bjgpopen.org/content/early/2025/03/22/BJGPO.2024.0300.full.pdf)

[^turn0search3]: NHS England. *Using an AI chatbot to streamline mental health referrals*. 2024. [Link](https://transform.england.nhs.uk/key-tools-and-info/digital-playbooks/workforce-digital-playbook/using-an-ai-chatbot-to-streamline-mental-health-referrals/)

[^CGAN]: Cai, Yingchao; Li, Mengxiao; Liu, Shiqi; Zhou, Changhao. *CycleGAN-based image translation from MRI to CT scans*. *Journal of Physics: Conference Series*, 2023. [Link](https://doi.org/10.1088/1742-6596/2646/1/012016)

[^topol2024]: Topol, Eric. *Generative AI in healthcare: friend or foe?* *Nature Medicine*, 2024. [Link](https://www.nature.com/articles/s41591-024-02887-2)

[^mathews2024]: Mathews, Andrew. *Digital twins and generative AI: The future of personalized medicine?* 2024. [Link](https://www.healthcareitnews.com/news/emea/digital-twins-and-generative-ai-future-personalized-medicine)

[^mayo2024]: Mayo Clinic. *How wearable devices are reshaping chronic disease care*. 2024. [Link](https://newsnetwork.mayoclinic.org/discussion/how-wearable-devices-are-reshaping-chronic-disease-care/)

[^acecf2024]: NHS England. *ACE-CF: Preventing hospital admissions in cystic fibrosis patients with AI-powered remote monitoring*. 2024. [Link](https://www.england.nhs.uk/long-read/ace-cf-cystic-fibrosis-remote-monitoring/)

[^cera2024]: Cera Care. *AI used to reduce hospital admissions in older adults by predicting falls and health deterioration*. 2024. [Link](https://www.ceracare.co.uk/news/ai-reduces-hospital-admissions-predicts-falls/)

[^uclforesight2024]: UCL Institute of Health Informatics. *Foresight: Transforming NHS care with generative AI*. 2024. [Link](https://www.ucl.ac.uk/health-informatics/news/2024/jan/foresight-transforming-nhs-care-generative-ai)
