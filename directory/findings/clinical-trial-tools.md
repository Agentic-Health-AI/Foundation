# Clinical Trial Tools - Open Source Directory

> Research date: 2026-02-26
> Part of the Agentic Health ecosystem research

---

## 1. Patient-to-Trial Matching Tools

### TrialGPT
- **URL**: https://github.com/ncbi-nlp/TrialGPT
- **Description**: End-to-end framework from NCBI/NLM for zero-shot patient-to-trial matching using large language models. Three modules: TrialGPT-Retrieval (large-scale filtering to retrieve candidate trials), TrialGPT-Matching (criterion-level patient eligibility prediction, 87.3% accuracy), and TrialGPT-Ranking (trial-level score generation). Retrieval module recalls over 90% of relevant trials using less than 6% of the initial collection.
- **Language**: Python
- **Relevance**: High. State-of-the-art LLM-based trial matching. Could serve as a core engine for patient-facing trial navigation in the Agentic Health ecosystem.

### MatchMiner
- **URL**: https://github.com/dfci/matchminer
- **Website**: https://matchminer.org/
- **Description**: Open-source computational platform from Dana-Farber Cancer Institute for matching patient-specific genomic profiles to precision cancer medicine clinical trials. Focuses on oncology genomic matching.
- **Language**: Python, JavaScript
- **Relevance**: High for oncology use cases. Demonstrates production-grade genomic trial matching.

### MatchMiner-AI
- **URL**: https://arxiv.org/abs/2412.17228
- **Description**: Extension of MatchMiner using AI for clinical trial search and ranking, trained entirely on synthetic EHR data. Model weights, inference tools, and demo frontends are publicly available. Published January 2026.
- **Relevance**: High. Shows how to train trial matching models on synthetic data, avoiding privacy issues.

### Clinical Trial Matching Engine (mcode)
- **URL**: https://github.com/mcode/clinical-trial-matching-engine
- **App**: https://github.com/mcode/clinical-trial-matching-app
- **Description**: SMART on FHIR application for matching patient records with clinical trials. Provides a uniform interface for connecting clinical trial matching services. Part of the mCODE (Minimal Common Oncology Data Elements) initiative.
- **Language**: TypeScript, JavaScript
- **Relevance**: High. FHIR-based approach enables integration with EHR systems. Standards-compliant design.

### TrialMatchAI
- **URL**: https://github.com/cbib/TrialMatchAI
- **Description**: AI-driven tool using LLMs, NLP, and Explainable AI (XAI) to match cancer patients to clinical trials based on genomic and clinical profiles. Focuses on transparent, personalized recommendations.
- **Language**: Python
- **Relevance**: Medium-high. XAI focus is valuable for building trust in AI-driven recommendations.

### Zero-shot Clinical Trial Matching (Stanford)
- **URL**: https://github.com/som-shahlab/clinical_trial_patient_matching
- **Website**: https://som-shahlab.github.io/clinical_trial_patient_matching-website/
- **Description**: Zero-shot clinical trial matching with LLMs from Stanford's Shah Lab. Achieved accuracy 0.87, sensitivity 0.85, specificity 0.89 using GPT-4.
- **Language**: Python
- **Relevance**: High. Demonstrates zero-shot approach requiring no training data.

### Automated Matching for Pediatric Leukemia (Chicago PCDC)
- **URL**: https://github.com/chicagopcdc/Automated-Matching-of-Patients-to-Clinical-Trials
- **Description**: Patient-centric NLP approach for automated matching of patients to clinical trials, focused on pediatric leukemia.
- **Language**: Python
- **Relevance**: Medium. Niche pediatric focus but demonstrates patient-centric matching design.

### Microsoft Clinical Trials Blueprint
- **URL**: https://techcommunity.microsoft.com/t5/healthcare-and-life-sciences/enable-ai-driven-clinical-trials-matching-with-an-open-source/ba-p/3890797
- **Description**: Open-source blueprint providing a Trial Matcher chatbot based on Azure Health Bot. Patients provide information and the system checks eligibility for potential trials. One-click deployment on Azure.
- **Relevance**: Medium. Azure-dependent but demonstrates conversational trial matching UX.

---

## 2. ClinicalTrials.gov API Wrappers and Search Tools

### pytrials
- **URL**: https://github.com/jvfe/pytrials
- **PyPI**: https://pypi.org/project/pytrials/
- **Description**: Python wrapper for the ClinicalTrials.gov API. Simple pip install, clean API for searching and retrieving trial data.
- **Language**: Python
- **Relevance**: High. Most popular and maintained Python wrapper for ClinicalTrials.gov.

### clinical-trials-api-wrapper
- **URL**: https://github.com/jrenewhite/clinical-trials-api-wrapper
- **Description**: Python wrapper for the ClinicalTrials.gov REST API version 2.0.0-beta2. Updated for the newer API version.
- **Language**: Python
- **Relevance**: High. Supports the newer v2 API.

### clinical_trials_python (Code for America)
- **URL**: https://github.com/codeforamerica/clinical_trials_python
- **Description**: Python API wrapper with search and download methods. Search results returned in ZIP file format.
- **Language**: Python
- **Relevance**: Medium. Older project but demonstrates civic tech approach.

### py-clinical-trials
- **URL**: https://github.com/p2/py-clinical-trials
- **Docs**: https://p2.github.io/py-clinical-trials/
- **Description**: Python 3 classes to handle clinical trial data from ClinicalTrials.gov and other services. Works off JSON data with TrialServer class for retrieval.
- **Language**: Python
- **Relevance**: Medium. Multi-source support is useful.

### clinicaltrialr (R)
- **URL**: https://github.com/serghiou/clinicaltrialr
- **Description**: R package to import study records from ClinicalTrials.gov.
- **Language**: R
- **Relevance**: Medium. Useful for R-based analysis pipelines.

### rclinicaltrials (R)
- **URL**: https://github.com/sachsmc/rclinicaltrials
- **Description**: R interface to the ClinicalTrials.gov API.
- **Language**: R
- **Relevance**: Medium. Alternative R interface.

---

## 3. EU Clinical Trials Register Tools

### ctrdata (R Package)
- **URL**: https://github.com/rfhb/ctrdata
- **Docs**: https://rfhb.github.io/ctrdata/
- **Description**: R package to retrieve and analyze clinical trials data from multiple public registers: EU CTIS (euclinicaltrials.eu), ClinicalTrials.gov, and ISRCTN. Most comprehensive multi-register tool available.
- **Language**: R
- **Relevance**: High. Cross-register support including EU CTIS is very valuable for European/Danish context.

### euclinicaltrials.py
- **URL**: https://github.com/JulHeg/euclinicaltrials.py
- **Description**: Python scraper for the EU Clinical Trial Information System (CTIS) at euclinicaltrials.eu. Since the CTIS has no public machine-readable API, this package facilitates web scraping of the database.
- **Language**: Python
- **Relevance**: High. Only Python tool for accessing the new EU CTIS database.

### eu-clinical-trials-scraper
- **URL**: https://github.com/bilalkamal/eu-clinical-trials-scraper
- **Description**: Python scraper for EU Clinical Trials Register. Fetches detailed trial information within a specified date range, compiles data into structured formats.
- **Language**: Python
- **Relevance**: Medium. Useful for batch data extraction from EU register.

### OpenTrials (Archived)
- **URL**: https://github.com/opentrials/opentrials
- **API**: https://github.com/opentrials/api
- **Description**: Collaborative open database for all available structured data and documents on clinical trials. Aggregated data from ClinicalTrials.gov, WHO ICTRP, and EU Clinical Trials Register. Note: Project is no longer active, all repositories archived.
- **Relevance**: Low-medium. Archived but the data model and approach are instructive.

---

## 4. Clinical Trial Data Analysis Frameworks

### Tri-AL
- **URL**: https://github.com/pouyan9675/Tri-AL
- **Paper**: https://www.sciencedirect.com/science/article/abs/pii/S0306437924001170
- **Description**: Open-source platform for visualization and analysis of clinical trials. Features information extraction, historical analysis, reporting, and a programmable module for ML models to extract disease-specific data from unstructured trial reports.
- **Language**: Python
- **Relevance**: High. Comprehensive analysis and visualization platform.

### Clinical Trial Risk Tool
- **URL**: https://github.com/fastdatascience/clinical_trial_risk
- **Description**: NLP-based tool from Fast Data Science for analyzing clinical trial protocols and assessing risk of trials ending uninformatively. Uses Python Dash frontend and Java Tika for PDF reading.
- **Language**: Python, Java
- **Relevance**: Medium-high. Unique risk assessment angle for trial protocols.

### OpenStudyBuilder (Novo Nordisk)
- **URL**: https://github.com/NovoNordisk-OpenSource/openstudybuilder-description
- **Website**: https://novo-nordisk.gitlab.io/nn-public/openstudybuilder/project-description/
- **Description**: Open-source project from Novo Nordisk for clinical study evaluations. Covers protocol development, CRF design, dataset creation, analysis, reporting, and submission to health authorities. Python web application on FastAPI with CRUD, access control, versioning, and workflows.
- **Language**: Python (FastAPI)
- **Relevance**: Very high. Danish/Nordic origin (Novo Nordisk). Comprehensive study lifecycle tool.

### rpact
- **URL**: https://www.rpact.org/
- **Description**: R package for confirmatory adaptive clinical trial design, simulation, and analysis. Covers group sequential and adaptive designs.
- **Language**: R
- **Relevance**: Medium. Statistical design tool, useful for trial planning.

### ClinicalTrials.gov Analysis
- **URL**: https://github.com/nk9/clinical-trials
- **Description**: Python-based analysis of ClinicalTrials.gov data with graph generation.
- **Language**: Python
- **Relevance**: Low-medium. Simple analysis scripts.

---

## 5. Eligibility Criteria Parsing and Screening Tools

### Clinical Trial Parser (Facebook/Meta Research)
- **URL**: https://github.com/facebookresearch/Clinical-Trial-Parser
- **Description**: Library for converting clinical trial eligibility criteria to machine-readable format. Contains CFG and IE parser models, annotated word labeling data, medical word embeddings and vocabulary tools. CFG model achieves precision >= 90% and recall >= 85%.
- **Language**: Go
- **Relevance**: High. Production-quality parser from Meta for structured eligibility criteria extraction.

### Criteria2Query (OHDSI)
- **URL**: https://github.com/OHDSI/Criteria2Query
- **Description**: Natural language interface to clinical databases for cohort definition. Parses freetext inclusion criteria and produces structured cohort definitions executable against OMOP CDM.
- **Language**: Python
- **Relevance**: High. OMOP CDM integration makes it interoperable with major clinical data warehouses.

### Chia Dataset
- **Paper**: https://www.nature.com/articles/s41597-020-00620-0
- **Description**: Large annotated corpus of clinical trial eligibility criteria. Useful as training/evaluation data for NLP models parsing trial criteria.
- **Relevance**: Medium-high. Important dataset for training eligibility parsing models.

---

## 6. Rare Disease Clinical Trial Tools

### Rare Disease Registry Framework (RDRF)
- **URL**: https://github.com/muccg/rdrf
- **Docs**: https://muccg.github.io/rdrf/
- **Description**: Open-source tool for creating web-based patient registries for rare diseases. Uses reusable Common Data Elements (CDEs) that can be created/loaded at runtime, enabling registry creation without code changes.
- **Language**: Python (Django)
- **Relevance**: High for rare disease context. Patient registries are key infrastructure for rare disease trial recruitment.

### ECRIN Rare Diseases Clinical Trials Toolbox
- **URL**: https://ecrin.org/rare-diseases-clinical-trials-toolbox
- **Website**: https://www.ejprarediseases.org/rare-diseases-clinical-trials-toolbox/
- **Description**: Practical toolbox for developers of rare disease clinical trials. Collects knowledge, experience, and resources for understanding regulations and requirements, with special focus on investigator-initiated trials. Part of the European Joint Programme on Rare Diseases.
- **Relevance**: High for European/Danish rare disease context. Not software but essential knowledge resource.

### SIMCor (Virtual Cohorts for In-Silico Trials)
- **URL**: https://github.com/ecrin-github/SIMCor
- **Paper**: https://www.nature.com/articles/s41598-025-99720-3
- **Description**: EU-Horizon funded open-source web application providing R-statistical environment for validation of virtual cohorts and in-silico trials. Particularly useful for rare diseases where patient populations are small.
- **Language**: R
- **Relevance**: High. In-silico trials are especially important for rare diseases with limited patients.

---

## 7. Clinical Trial Recruitment Tools

### recruIT
- **Paper**: https://www.sciencedirect.com/science/article/pii/S0010482524004955
- **Description**: Cloud-native clinical trial recruitment support system based on HL7 FHIR and OMOP CDM. Generates automatic recruitment recommendations. Standards-based approach for integration with hospital systems.
- **Relevance**: High. FHIR + OMOP standards make it highly interoperable.

### OpenClinica
- **URL**: https://github.com/OpenClinica/OpenClinica
- **Website**: https://www.openclinica.com/
- **Description**: First commercial open-source clinical trial software for Electronic Data Capture (EDC) and Clinical Data Management (CDM). Includes recruitment solution (Recruit module).
- **Language**: Java
- **Relevance**: Medium. Established EDC platform, though recruitment module is commercial.

### LibreClinica
- **Description**: Community-driven successor of OpenClinica. Open-source EDC and CDM software.
- **Relevance**: Medium. Fully open-source alternative to OpenClinica.

---

## 8. Danish and Nordic Clinical Trial Resources

### Trial Nation
- **URL**: https://trialnation.dk/
- **Description**: Single national entry point for conducting clinical trials in Denmark. Services include investigator identification, coordinated feasibility process with national hospital response, patient number estimation, and access to partnerships with hospitals, scientists, and patient networks. Free of charge.
- **Relevance**: Very high. Central Danish infrastructure for clinical trials.

### Copenhagen Trial Unit (CTU)
- **URL**: https://ctu.dk/
- **Description**: Clinical intervention research unit conducting research across all specialties. Involved in 168+ randomized clinical trials with 135,000+ participants. Provides expertise in planning, conduct, analysis, and interpretation of RCTs.
- **Relevance**: Very high. Key Danish institution for clinical trial methodology.

### Aarhus University Clinical Trial Candidate Database
- **Paper**: https://pmc.ncbi.nlm.nih.gov/articles/PMC3986109/
- **Description**: Database of encrypted data from the Danish National Registry of Patients enabling estimation of patient numbers with specific discharge diagnoses across hospital departments in Central Denmark Region.
- **Relevance**: High. Danish-specific feasibility assessment tool.

### Danish Medicines Agency (Laegemiddelstyrelsen) - Clinical Trials
- **URL**: https://laegemiddelstyrelsen.dk/en/licensing/clinical-trials/
- **Description**: Regulatory authority for clinical trials with medicinal products in Denmark. Published DCT (Decentralized Clinical Trials) guideline in 2021.
- **Relevance**: High. Regulatory reference for Danish clinical trials.

### OpenStudyBuilder (Novo Nordisk)
- **URL**: https://github.com/NovoNordisk-OpenSource/openstudybuilder-description
- **Description**: (See Section 4 above.) Danish pharma company's open-source study lifecycle tool.
- **Relevance**: Very high. Danish-origin open-source clinical trial tool.

---

## 9. Clinical Data Standards and Infrastructure

### ClinicalDataSources
- **URL**: https://github.com/EpistasisLab/ClinicalDataSources
- **Description**: Curated list of open or easy-access clinical data sources for biomedical research from the Epistasis Lab.
- **Relevance**: Medium. Useful reference for finding training data.

### OHDSI/OMOP CDM
- **Description**: Observational Medical Outcomes Partnership Common Data Model. Standard data model used by many tools above (Criteria2Query, recruIT). Not a single tool but a critical standard for clinical data interoperability.
- **Relevance**: High. Key data standard underpinning many clinical trial tools.

---

## Summary and Recommendations for Agentic Health

### Highest Priority Tools
| Tool | Why |
|------|-----|
| **TrialGPT** | Best-in-class LLM-based trial matching, open source, from NIH/NLM |
| **OpenStudyBuilder** | Danish origin (Novo Nordisk), comprehensive study lifecycle |
| **ctrdata** | Multi-register support including EU CTIS, essential for Danish/EU trials |
| **euclinicaltrials.py** | Only Python scraper for new EU CTIS, essential for European context |
| **pytrials** | Clean Python wrapper for ClinicalTrials.gov API |
| **Clinical Trial Parser (Meta)** | Production-quality eligibility criteria parser |
| **RDRF** | Open-source rare disease registry framework |

### Key Integration Opportunities
1. **TrialGPT + pytrials + euclinicaltrials.py**: Build a multi-registry trial matching pipeline covering both US and EU trials
2. **Clinical Trial Parser + Criteria2Query**: Parse eligibility criteria into structured queries against clinical databases
3. **ctrdata + Tri-AL**: Cross-register data retrieval with visualization and analysis
4. **RDRF + TrialGPT**: Rare disease patient registry with AI-powered trial matching
5. **OpenStudyBuilder**: Study design and protocol management, Danish ecosystem integration

### Danish/Nordic Ecosystem
- Trial Nation and CTU are key institutional partners
- OpenStudyBuilder from Novo Nordisk provides Danish pharma industry alignment
- Danish national registries (via Aarhus database) enable unique feasibility assessment
- EU CTIS tools essential as Denmark transitions to EU clinical trial regulation
