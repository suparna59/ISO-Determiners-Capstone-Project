# ISO Determiners  
**Semi-automated Determination System for Illicit Synthetic Opioid Tracking**

This project was developed as part of the DAEN-690 Capstone at George Mason University (Spring 2025). It aims to provide regulatory agencies and law enforcement with a transparent, evidence-backed, and tunable system to monitor and prioritize high-risk entities in the illicit synthetic opioid (ISO) supply chain.

---

## Team Members  
- Bhargav Dasari  
- Sagarika Komati Reddy  
- Venkata Krishna Kothapalli  
- Suparna Mannava  
- Uday Madivada  
- Kamani Madasu  

---

## Project Overview  
The ISO Determination Engine is a semi-automated framework designed to assist in identifying companies and chemicals involved in fentanyl trafficking. It supports analysts and investigators through:

- Adjustable risk scoring models  
- A centralized platform for tagging supporting evidence  
- Automated extraction of entities (people, companies, chemicals)  
- Dashboards providing real-time risk insights  

---

## Problem Statement  
Over 70,000 deaths occur annually in the U.S. due to synthetic opioids like fentanyl. The illicit supply chain is often obscured by legitimate business operations, making detection and intervention difficult.

### Limitations of Current Tools:  
- Lack of automation  
- Poor evidence traceability  
- Rigid scoring methods  

### Our Solution:  
The ISO Determination Engine is a semi-automated system that combines entity recognition, manual tagging, and risk scoring to evaluate the potential complicity of companies and chemicals involved in fentanyl production.

---

## Solution Approach  

### Modular Pipeline:
1. **Document Ingestion** – Ingest press releases, sanctions, indictments  
2. **Entity Recognition** – Extract chemical names and company aliases  
3. **Evidence Tagging** – Manual tagging of supporting evidence  
4. **Risk Scoring Model** – Configurable formula for risk scoring  
5. **Interactive Dashboard** – Real-time visualization of risk scores and trends  
6. **Clustering Analysis** – Unsupervised learning to detect suspicious networks  

This approach enables analysts to prioritize cases, trace decisions to specific evidence, and configure the system as needed.

---

## Datasets Used  

| Dataset               | Source  | Description                                                |
|-----------------------|---------|------------------------------------------------------------|
| DOJ Indictments       | USDOJ   | Press releases and case details of fentanyl-related cases  |
| DEA SSL               | DEA     | List of scheduled precursor chemicals                      |
| Company Reference Sheet | Curated | PRC-linked companies, aliases, sanctions, and subsidies   |

---

## Weighted Risk Scoring Model  

**Formula:**  
`Total Score = (Sanctions × 1.2) + (Subsidies × 1.1) + (Complicity × 1.3)`

| Component   | Description                                      | Weight |
|-------------|--------------------------------------------------|--------|
| Sanctions   | Legal actions against the entity                 | 1.2    |
| Subsidies   | Government affiliations possibly aiding ISO trade | 1.1    |
| Complicity  | Behavioral or contextual red flags               | 1.3    |

> All weights are adjustable via the Streamlit interface.

---

## Key Features  
- **Risk Scoring Engine** – Transparent and tunable scoring  
- **Evidence Tagging** – Manual tagging for reliability  
- **Entity Recognition** – NLP-powered extraction of relevant entities  
- **Interactive Dashboard** – Exportable, filterable risk views  
- **Clustering Analysis** – K-means clustering to find hidden relationships  

---

## Limitations & Future Work  
- Manual tagging is labor-intensive; plans for NLP confidence thresholds and pre-trained models are underway  
- OCR tools (e.g., AWS Textract) have limitations with complex PDF layouts  
- Future versions aim to automate evidence extraction and integrate real-time court document scraping  

---

## References  
- Select Committee on the CCP  
- TraCCC Research  
- CDC Report on Fentanyl  

---

## ⚠Disclaimer  

Sensitive datasets used in this project are **not included** in this public repository due to privacy and institutional restrictions.

