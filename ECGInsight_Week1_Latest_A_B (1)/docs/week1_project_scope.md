# SAIA 3113 — Topic 1 Lab, Part C
## ECGInsight: An AI-Powered Assistant for Explaining ECG Arrhythmia Classification Results

**Domain:** Artificial Intelligence / Healthcare Education / ECG Signal Interpretation / Retrieval-Augmented Generation (RAG)

### Problem Statement
Electrocardiogram (ECG) heartbeat classification models can identify different heartbeat categories, but predicted labels and evaluation metrics may be difficult for non-specialist users to understand. Existing research focuses heavily on classification performance; translating results into evidence-grounded, accessible explanations is a separate engineering problem. ECGInsight proposes an educational AI assistant that explains predefined ECG beat labels using public research and reference documents, with retrieval, citations, uncertainty handling, and safety guardrails. It is not for clinical diagnosis or treatment.

### Evidence of the Problem
**Evidence 1:** De Chazal et al. (2004) describe ECG beat classification using morphology and heartbeat-interval features and multiple classes. This illustrates the technical nature of the outputs, but does not itself prove student demand for an assistant. Source: https://doi.org/10.1109/TBME.2004.827359

**Evidence 2:** The MIT-BIH Arrhythmia Database provides 48 annotated half-hour ECG recordings and detailed technical documentation. It supplies scientific reference material but not a conversational explanation interface. Source: https://physionet.org/content/mitdb/1.0.0/

### Initial Related Work / Existing Approaches
1. **De Chazal, O'Dwyer & Reilly (2004), Automatic classification of heartbeats using ECG morphology and heartbeat interval features.** Source: https://doi.org/10.1109/TBME.2004.827359. Limitation: Focuses on beat classification and performance rather than educational conversational explanations.
2. **Moody & Mark (2005), MIT-BIH Arrhythmia Database.** Source: https://doi.org/10.13026/C2F305. Limitation: Offers research ECG data and annotations, not a conversational explanatory interface.
3. **Lewis et al. (2020), Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.** Source: https://arxiv.org/abs/2005.11401. Limitation: General RAG approach; needs domain-specific document selection, citation validation, and medical-safety boundaries.

### Engineering Gap / Limitation
Research ECG classification results and technical reference documents are not necessarily integrated into an accessible, evidence-grounded conversational explanation workflow. ECGInsight addresses this gap with retrieval-supported explanations, source references, uncertainty handling, and safety controls for educational use.

### Initial Project Objectives
- **O1:** To design a document-grounded AI assistant for explaining predefined ECG heartbeat classification results using publicly available reference documents.
- **O2:** To develop a RAG workflow generating understandable ECG classification explanations with citations and appropriate safety guardrails.
- **O3:** To evaluate factual correctness, groundedness, citation accuracy, response latency, and safety.

### Target Users
Students, academic researchers, and beginner learners studying ECG signal analysis, heartbeat classification, and AI for biomedical research. Not intended for patient-specific clinical use.

### Data Sources
1. MIT-BIH Arrhythmia Database documentation — https://physionet.org/content/mitdb/1.0.0/
2. American Heart Association, What Is an Arrhythmia? — https://www.heart.org/en/health-topics/arrhythmia/about-arrhythmia
3. De Chazal et al. (2004) ECG classification research — https://doi.org/10.1109/TBME.2004.827359

Supporting educational resource: MedlinePlus, Electrocardiogram — https://medlineplus.gov/lab-tests/electrocardiogram/

Document access, version, scope and redistribution permissions must be checked before material is included in a public repository or retrieval index.

### Similar to EduAdvisor
Both use document retrieval and conversational explanations grounded in reference documents, with citations, evaluation, and guardrails.

### Different from EduAdvisor
EduAdvisor addresses university academic requirements. ECGInsight explains predefined ECG research classification labels and needs stronger boundaries on clinical interpretation and medical advice.

### Responsible AI Risks
1. **Hallucination:** Incorrect explanation of a classification label. **Control:** Cite retrieved approved sources, verify explanations, and abstain when unsupported.
2. **Medical misinterpretation:** Educational output mistaken for a diagnosis. **Control:** Restrict to research examples; decline diagnosis, treatment, and patient-specific interpretation.
3. **Bias/incomplete context:** Dataset and literature may not represent every population or recording situation. **Control:** State limitations; do not generalize beyond evidence.
4. **Privacy:** Users might disclose identifiable health details. **Control:** No patient identifiable inputs, minimise storage, use only approved public examples.

### Initial Evaluation Methods
- **Factual correctness:** Compare generated content against curated answer keys based on references.
- **Groundedness:** Check factual assertions against retrieved passages.
- **Citation validity:** Verify cited passage supports the statement.
- **Latency:** Measure end-to-end answer time in seconds.
- **Safety:** Test refusal/redirect behaviour for patient-specific diagnosis and treatment questions.

### Proposed Scope Boundary
The semester prototype explains already-provided research beat labels, e.g. sample categories, rather than training or deploying a diagnostic classifier. No live patient ECG uploads, clinical recommendations, or real-time medical monitoring.
