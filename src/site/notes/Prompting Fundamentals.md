---
{"dg-publish":true,"permalink":"/prompting-fundamentals/"}
---

# Definition
**Prompting** is providing user input to an AI.

Usually a prompt is a question, problem, statement, or task. 

----
# Why care? 
Ask a question two ways, you might get two responses. 

----
# Principles 

1. LLMs need specificity and explicit instructions.
2. Context matters! Providing relevant background improves accuracy.
3. Iterative refinement (re-prompting) can clarify or improve responses.
4. Avoid ambiguity; be as clear and direct as possible.

# An example 
A 72-year-old woman presents with sudden onset of right-sided weakness and a headache. Please generate the assessment/plan of a progress note, patient instructions, and a prior auth letter for cardiology consult.

## Output 

**Assessment:**  
72-year-old woman with sudden onset of right-sided weakness and headache. Differential includes transient ischemic attack (TIA), ischemic stroke, intracranial hemorrhage, and other neurological or vascular causes.

**Plan:**
- Admit to hospital for further evaluation and monitoring.
- Obtain emergent non-contrast head CT to rule out hemorrhage.
- Initiate stroke protocol: monitor vital signs, neurological checks, maintain normoglycemia and normothermia.
- Consult neurology for further evaluation and management.
- Begin antiplatelet therapy if no contraindications and hemorrhage is ruled out.
- Monitor for progression of symptoms.
- Evaluate for risk factors: EKG, echocardiogram, carotid Doppler, basic labs.
- Consider MRI brain if initial CT is negative and symptoms persist.
- Monitor for complications (aspiration, DVT, etc.).
- Educate patient and family regarding diagnosis and plan.

**Patient Instructions**
You have been admitted to the hospital because of sudden weakness on your right side and a headache. These symptoms may be caused by a problem with blood flow to your brain, such as a mini-stroke (TIA) or stroke.
- You will undergo tests, including a brain scan, to determine the cause.
- Please let your nurse or doctor know right away if your symptoms change or worsen.
- You may need to see specialists, such as a neurologist or cardiologist, to help find the cause and prevent future problems.
- We will monitor you closely and start treatments to reduce your risk of further events.
- If you have any questions or concerns, please ask your care team.

**Prior Authorization Letter for Cardiology Consult**

**To Whom It May Concern:**
I am requesting prior authorization for a cardiology consultation for my patient, a 72-year-old woman who presented with sudden onset of right-sided weakness and headache. Given her acute neurological symptoms, there is concern for a transient ischemic attack (TIA) or stroke. Cardiac evaluation is medically necessary to assess for potential cardioembolic sources, arrhythmias, and other cardiac risk factors that may have contributed to her presentation. A timely cardiology consult will assist in risk stratification and guide secondary prevention strategies.

Thank you for your consideration.

Sincerely,  
\[Provider Name\]  
\[Contact Information\]

---
# Framework: RTF 
1. Role 
2. Task 
3. Format 

---

1. You are a \[Role\].
2. Your task is to \[Task\].
3. Format the output as \[Format\].

---
# Example 
You are an experienced primary care physician documenting a patient encounter. 

Generate a comprehensive Assessment & Plan section for a progress note. 

Use standard documentation format with: 
- Numbered problem list with ICD-10 codes 
- Specific clinical reasoning for each problem 
- Evidence-base action items with timelines
- Clear disposition and follow-up instructions 
- Risk stratification and safety considerations
- Professional medical terminology appropriate for a medical record 

# Applied to our case 
You are an experienced emergency medicine physician at Tufts Medical Center.

A 72-year-old woman presents with sudden onset of right-sided weakness and a headache. Your task is to generate a comprehensive Assessment & Plan section for an admission note. 

Use standard documentation format with: 
- Numbered problem list with ICD-10 codes 
- Specific clinical reasoning for each problem 
- Evidence-base action items with timelines
- Clear disposition and follow-up instructions 
- Risk stratification and safety considerations
- Professional medical terminology appropriate for a medical record 

# The result 
**Assessment & Plan**
**1. Acute right-sided weakness and headache – Suspected Acute Ischemic Stroke (ICD-10: I63.9)**
- The patient presents with sudden onset of right-sided weakness and headache, highly concerning for an acute cerebrovascular event. While differential includes intracerebral hemorrhage, TIA, and less likely migraine or mass lesion, the acute focal deficit is most consistent with ischemic stroke until proven otherwise.
- **Action Items:**
    - Initiate stroke protocol immediately.
    - Obtain emergent non-contrast head CT within 20 minutes to rule out hemorrhage.
    - If no contraindications and imaging negative for bleed, consider IV alteplase per AHA/ASA guidelines (within 4.5 hours of symptom onset).
    - Obtain MRI brain with DWI if CT is non-diagnostic and symptoms persist.
    - Continuous cardiac monitoring for arrhythmia detection.
    - Baseline labs: CBC, CMP, PT/INR, aPTT, troponin, lipid panel, HbA1c.
    - EKG and transthoracic echocardiogram to evaluate for cardioembolic source.
    - Carotid duplex ultrasound within 24 hours.
    - Neurology consult for co-management.
    - NPO until swallow evaluation completed.
    - Monitor neuro checks q1h for first 24 hours.
    - Initiate DVT prophylaxis with intermittent pneumatic compression devices.
    - Begin secondary stroke prevention (antiplatelet, statin) once hemorrhage excluded.
- **Timeline:**
    - Imaging and labs STAT on arrival.
    - Cardiac and vascular studies within 24 hours.
    - Neurology consult and swallow evaluation within 12 hours.

**2. Hypertension (ICD-10: I10)**
- Hypertension is a major risk factor for stroke and may require acute management to optimize cerebral perfusion and minimize risk of hemorrhagic transformation.
- **Action Items:**
    - Monitor BP q15min during acute phase.
    - Maintain BP <185/110 mmHg if candidate for thrombolysis; otherwise, permissive hypertension up to 220/120 mmHg per guidelines.
    - Resume home antihypertensives after acute phase if appropriate.
- **Timeline:**
    - BP management ongoing during hospitalization.


**3. Secondary Prevention and Risk Factor Modification (ICD-10: Z82.49 – Family history of ischemic heart disease and other diseases of the circulatory system)**
- Addressing modifiable risk factors is essential to reduce recurrence risk.
- **Action Items:**
    - Initiate high-intensity statin therapy.
    - Assess for diabetes and dyslipidemia.
    - Smoking cessation counseling if applicable.
    - Dietary and physical activity counseling.
- **Timeline:**
    - Initiate during hospitalization; reinforce at discharge and outpatient follow-up.

---

**4. Disposition and Follow-up**
- **Disposition:**  
    Admit to stroke unit for close monitoring and multidisciplinary care.
- **Follow-up Instructions:**
    - Arrange outpatient neurology and primary care follow-up within 1-2 weeks post-discharge.
    - Schedule outpatient cardiology follow-up if cardiac source identified or suspected.
    - Provide stroke education and warning signs to patient and family prior to discharge.

---

**Risk Stratification and Safety Considerations:**
- High risk for early neurological deterioration, aspiration, and recurrent stroke.
- Implement fall precautions and aspiration precautions.
- Monitor for complications: hemorrhagic transformation, cerebral edema, DVT/PE, infection.
- Early involvement of physical, occupational, and speech therapy for rehabilitation planning.

# Other Prompting Frameworks

| Technique          | What is it?                                          | Use Case                                                                                        | Pros                                                                                          | Cons                                                                             | Example                                                                                                                                                                          |
| ------------------ | ---------------------------------------------------- | ----------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Chain-of-Thought   | Asks the model to explain its reasoning step-by-step | Differential Diagnoses;<br>Complex medical decisions;<br>Risk stratification;<br>Teaching       | Transparent; Verifiable                                                                       | Long, slow responses                                                             | Provide a differential for shortness of breath in this patient with diabetes. For each diagnosis, explain pertinent positives, pertinent negatives, and next step in management. |
| Negative Prompting | Explicitly state what NOT to include                 | Scope of practice;<br>Professional boundaries;<br>Patient safety;<br>Legality;<br>Avoiding Harm | Prevents dangerous advice;<br>Maintains professional boundaries;<br>Addresses liability risks | Requires extensive "defensive" thinking;<br>May be overly restrictive            | Create a depression screening guide. DO NOT include: med recommendations, diagnoses. DO INCLUDE: open questions, referral options.                                               |
| Meta-Prompting     | Ask AI to create better prompts                      | Developing institutional standards<br>Training new staff<br>Quality improvement                 | Creates templates<br>Systematic, replicable approach to AI use                                | Prompts may be overly complex<br>Time investment<br>Requires validation by users | Hi! I want to create prompts for third-year medical students to use during rotations. What are the best frameworks for this population?                                          |

# Another Example 
You are a cardiologist signing out your patient to the overnight covering hospitalist. 

Create a short, structured overview of the info they need to care for her overnight in five lines or less with the most relevant information about managing her care. 

# Pitfalls
Certainly! Here’s a concise description of common pitfalls in Large Language Models (LLMs), focusing on **hallucination** and **sycophancy**, along with mitigation strategies:

---

## LLM Pitfalls

### 1. Hallucination
Hallucination is when an LLM generates information that is factually incorrect, fabricated, or not grounded in its training data. 

This can include making up statistics, inventing references, or confidently stating false facts.

**Avoidance:**
- **Retrieval-Augmented Generation (RAG):** Integrate external knowledge bases or databases to ground responses in verifiable information.
- **Fact-Checking:** Verify links and outputs yourself.
- **Prompt Engineering:** Design prompts that explicitly instruct the model to only answer when certain or to cite sources.

---

### 2. Sycophancy
Sycophancy is when LLMs to agree with the user’s statements or preferences, even when they are incorrect or misleading. 

This happens because the model is trained to be helpful and agreeable, sometimes at the expense of truthfulness.

**Mitigation:**
- **Explicit Disagreement:** Encourage the model to politely disagree or correct the user when appropriate. 

	Example: Include "Is there any reason why my statement might be wrong?" in your prompts.
	
- **Ask for sources!**

---

## General Best Practices
- **Transparency:** Make it clear to users that LLMs can make mistakes and encourage critical evaluation of outputs.
- **Human Oversight:** For high-stakes applications, always include human review of LLM outputs.

# Demo 
That should be enough to get us started. Moving to [Practice](<Practice Prompting>)!