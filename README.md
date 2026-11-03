# ECGInsight — AI-Powered ECG Classification Explanation Assistant

> An educational document-grounded AI assistant explaining predefined ECG heartbeat classification results with research-based citations. Not a medical diagnosis or treatment tool.

## Problem Statement
ECG beat classification results can be technical and difficult for learners to interpret. ECGInsight proposes a retrieval-augmented conversational interface explaining predefined research labels using verified documents and clearly communicating uncertainty and limitations.

## Evidence of the Problem
- De Chazal et al. (2004) demonstrate a technically detailed ECG heartbeat classification task: https://doi.org/10.1109/TBME.2004.827359
- The MIT-BIH Arrhythmia Database publishes extensive annotated ECG data and technical documentation, but is not a conversational explanation service: https://physionet.org/content/mitdb/1.0.0/

## Initial Related Work / Existing Approaches
1. **De Chazal et al. (2004)** — ECG beat classification research; lacks a learner-focused conversational explanation interface. https://doi.org/10.1109/TBME.2004.827359
2. **Moody & Mark (2005), MIT-BIH** — ECG reference data and annotations; no conversational assistant. https://doi.org/10.13026/C2F305
3. **Lewis et al. (2020), RAG** — retrieval-grounded generation method; needs domain-specific safety and verification. https://arxiv.org/abs/2005.11401

## Engineering Gap / Limitation
A narrow, reference-grounded educational explanation workflow with accurate citations and non-diagnostic safety boundaries is not provided by the dataset or baseline classification studies alone.

## Project Objectives
- O1: Design a document-grounded AI assistant for explaining predefined ECG heartbeat classification results.
- O2: Develop RAG explanations with source citations and safety guardrails.
- O3: Evaluate correctness, groundedness, citation validity, latency, and safety.

## Target Users
Students, researchers, and beginners learning ECG classification; not clinical patients.

## Data Sources
- MIT-BIH Arrhythmia Database: https://physionet.org/content/mitdb/1.0.0/
- American Heart Association — What Is an Arrhythmia?: https://www.heart.org/en/health-topics/arrhythmia/about-arrhythmia
- De Chazal et al. (2004): https://doi.org/10.1109/TBME.2004.827359

## Responsible AI and Scope
Research and educational use only. Do not use for diagnosis or treatment. Do not submit personal health data. Source permissions and versions will be checked before ingestion.

## Weekly Progress
| Week | Focus | Deliverable | Status |
|---|---|---|---|
| W1 | Initial system map, project scope | README + docs | Prepared locally — GitHub upload pending |

## Repository Structure
- `docs/` — week 1 observation sheet, system map, project scope
- `data/` — permitted data references only
- `src/` — application source code
- `notebooks/` — experiments
- `evaluation/` — tests and results
- `prompts/` — prompt configurations

## Week 1 Evidence
- `docs/week1_observation_sheet.md` — Part A observations from the 5-person group (with the latest source PDF retained in `original_reports/`).
- `docs/week1_system_map.png` — Part B diagram extracted from the latest Part B group report.
- `docs/week1_project_scope.md` — individual ECGInsight project scope.

Note: The Part A group-sharing reflection still requires one observation from another group, as specified by the lab.
