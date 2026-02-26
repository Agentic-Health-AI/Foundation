# Danish Open-Source Health AI Projects

Research compiled: 2026-02-26

---

## Government & National Health Authority Projects

### Sundhedsdatastyrelsen (Danish Health Data Authority)
- **URL:** https://github.com/Sundhedsdatastyrelsen
- **Description:** The Danish Health Data Authority's GitHub organization with 7+ public repositories covering national health IT infrastructure.
- **Relevance:** Core Danish government health data authority; sets the standard for digital health infrastructure in Denmark.

### Sundhedsdatastyrelsen/ehdsi
- **URL:** https://github.com/Sundhedsdatastyrelsen/ehdsi
- **Description:** Danish implementation of MyHealth @ EU -- eHealth Digital Service Infrastructure (eHDSI). Facilitates cross-border exchange of health data including patient summaries and e-prescriptions across the EU.
- **Relevance:** Shows how Denmark implements EU-wide health data exchange standards; relevant for cross-border health AI interoperability.

### Sundhedsdatastyrelsen/Smittestop.Mobile
- **URL:** https://github.com/Sundhedsdatastyrelsen (repository within org)
- **Description:** Danish mobile application for COVID-19 spread tracking, written in C#. Published for transparency.
- **Relevance:** Example of Danish government open-sourcing a public health application.

### Sundhedsdatastyrelsen/Coronapas.Mobile
- **URL:** https://github.com/Sundhedsdatastyrelsen/Coronapas.Mobile
- **Description:** Source code of the Danish Coronapas (COVID passport) app, published for reference and transparency.
- **Relevance:** Demonstrates Danish public-sector approach to transparent health app development.

### Sundhedsdatastyrelsen/epps-bootstrap-poc
- **URL:** https://github.com/Sundhedsdatastyrelsen/epps-bootstrap-poc
- **Description:** Proof-of-concept for the ePrescription & Patient Summary Project enabling requests from foreign health professionals in other EU member states.
- **Relevance:** Cross-border health data exchange PoC relevant to EU health data interoperability.

---

## HL7 FHIR Danish Profiles & Standards

### hl7dk/dk-core
- **URL:** https://github.com/hl7dk/dk-core
- **Description:** Danish HL7 FHIR core profiles (DK Core). Defines fundamental FHIR profiles for Denmark that other Danish health IT systems inherit from. Managed by the HL7 Danish FHIR working group.
- **Relevance:** The foundational FHIR standard for all Danish health IT; essential for any health AI project needing to exchange structured health data in Denmark.

### hl7dk (HL7 Denmark organization)
- **URL:** https://github.com/hl7dk
- **Description:** HL7 Denmark's GitHub organization containing multiple Danish FHIR implementation guides and profiles.
- **Relevance:** Central hub for Danish health interoperability standards.

### hl7dk/KL-dk
- **URL:** https://github.com/hl7dk/KL-dk
- **Description:** Local Government Denmark (Kommunernes Landsforening) HL7 FHIR profiles for municipal health and social care data exchange.
- **Relevance:** Defines how Danish municipalities exchange health data; important for community health AI applications.

### hl7dk/KL-dk-tools
- **URL:** https://github.com/hl7dk/KL-dk-tools
- **Description:** Observations and questionnaires used in Danish municipalities, implementing FKI (Faelleskommunal InformationsModel) FHIR profiles.
- **Relevance:** Standardized health assessment tools used across Danish municipalities.

### hl7dk/kl-children
- **URL:** https://github.com/hl7dk/kl-children
- **Description:** Implementation guide for municipality health prevention for children in Denmark.
- **Relevance:** FHIR profiles specifically for child health prevention data in Danish municipalities.

### hl7dk/kl-gateway-municipality-care-data
- **URL:** https://github.com/hl7dk/kl-gateway-municipality-care-data
- **Description:** Implementation guide for delivery of care data from KL Gateway, covering health and eldercare data reporting.
- **Relevance:** Gateway for municipal care data exchange; relevant for eldercare and home care AI applications.

### hl7dk/kl-ffb-reporting
- **URL:** https://github.com/hl7dk/kl-ffb-reporting
- **Description:** FHIR implementation guide for reporting FFB (social care) data to a gateway.
- **Relevance:** Social care data reporting standards for Danish municipalities.

---

## MedCom FHIR Standards

### medcomdk/dk-medcom-core
- **URL:** https://github.com/medcomdk/dk-medcom-core
- **Description:** MedCom Core profiles (Kerneprofiler) describing fundamental information for health data exchange in Denmark. MedCom is a non-profit owned by the Ministry of Health, Danish Regions, and Local Government Denmark.
- **Relevance:** Core messaging profiles used across the entire Danish healthcare system.

### medcomdk/dk-medcom-messaging
- **URL:** https://github.com/medcomdk/dk-medcom-messaging
- **Description:** MedCom messaging profiles for FHIR-based health message exchange in Denmark.
- **Relevance:** Defines the messaging framework for Danish healthcare communication.

### medcomdk/dk-medcom-carecommunication
- **URL:** https://github.com/medcomdk/dk-medcom-carecommunication
- **Description:** FHIR profiles for the CareCommunication standard used in Danish healthcare.
- **Relevance:** Standard for care communication between Danish health providers.

### medcomdk/dk-medcom-hospitalnotification
- **URL:** https://github.com/medcomdk/dk-medcom-hospitalnotification
- **Description:** FHIR profiles for hospital notification standards in Denmark.
- **Relevance:** Standardized hospital admission/discharge notifications.

### medcomdk/dk-medcom-acknowledgement
- **URL:** https://github.com/medcomdk/dk-medcom-acknowledgement
- **Description:** The Acknowledgement FHIR standard (Kvittering) for receipt confirmation of delivered MedCom messages.
- **Relevance:** Message delivery confirmation infrastructure for Danish health messaging.

---

## Telemedicine & FUT Infrastructure

### trifork/fut-web-client
- **URL:** https://github.com/trifork/fut-web-client
- **Description:** Web client for the FUT (Faelles Udbredelse af Telemedicin) infrastructure, showcasing parts of the FUT API. FUT is Denmark's national telemedicine platform offering single sign-on and a secured HL7 FHIR API.
- **Relevance:** Reference implementation for Denmark's national telemedicine infrastructure; demonstrates how to build apps on top of FUT.

### trifork/fhir-validator
- **URL:** https://github.com/trifork/fhir-validator
- **Description:** A dockerized version of the FHIR validator, developed by Trifork (Danish health tech company).
- **Relevance:** Useful tool for validating FHIR resources against Danish profiles.

### trifork/hapi-fhir-export-client
- **URL:** https://github.com/trifork/hapi-fhir-export-client
- **Description:** Library for HAPI FHIR Bulk data export.
- **Relevance:** Tool for bulk health data export from FHIR servers.

### trifork/fhir-ig-sample
- **URL:** https://github.com/trifork/fhir-ig-sample
- **Description:** Sample FHIR Implementation Guide project by Trifork.
- **Relevance:** Template for creating Danish FHIR implementation guides.

### OpenTele (4S Foundation)
- **URL:** https://github.com/4s (referenced; check medfloss.org/node/935 for links)
- **Description:** Open-source home healthcare monitoring platform developed for Danish telemedicine. Uses HL7 standards, runs on Apache Tomcat, released under Apache 2.0 license. Commissioned by government-funded projects (CIH/TelecareNorth). Members include Denmark's eHealth authority, three Danish regions, municipalities, Aarhus University, and the Alexandra Institute.
- **Relevance:** Major Danish open-source telemedicine platform used for chronic disease monitoring (diabetes, lung disease) and complicated pregnancies.

---

## University & Research Projects

### hds-sandbox (Health Data Science Sandbox)
- **URL:** https://github.com/hds-sandbox
- **Description:** Collaborative project coordinated by the Center for Health Data Science at the University of Copenhagen (KU), with participants from DTU, SDU, and AU. Provides educational materials and tools for health data science. Funded by the Novo Nordisk Foundation (grant NNF20OC0063268). Hosted on Danish supercomputers Computerome and UCloud.
- **Relevance:** Multi-university Danish initiative providing open-source training materials for health data science; directly relevant for building health AI capacity.

### hds-sandbox/GWAS_course
- **URL:** https://github.com/hds-sandbox/GWAS_course
- **Description:** Genome-Wide Association Studies course material covering population genetics concepts and GWAS principles.
- **Relevance:** Open educational resources for genomic health research in Denmark.

### hds-sandbox/bulk_RNAseq_course
- **URL:** https://github.com/hds-sandbox/bulk_RNAseq_course
- **Description:** Bulk RNA-seq course from the Danish Health Data Science Sandbox project, covering read preprocessing, normalization, differential expression analysis, and gene annotation.
- **Relevance:** Bioinformatics training relevant to Danish health research.

### hds-sandbox/AlphaFold_Workshop
- **URL:** https://github.com/hds-sandbox/AlphaFold_Workshop
- **Description:** Workshop for protein folding prediction using ColabFold, AlphaFold2, and MMseqs2. Designed to run on UCloud.
- **Relevance:** AI-driven protein structure prediction resources for Danish researchers.

### Pioneer Centre for AI
- **URL:** https://github.com/Pioneer-Centre-for-AI
- **Description:** GitHub organization for the Pioneer Centre for Artificial Intelligence, based at University of Copenhagen's Department of Computer Science. Collaborates with DTU, ITU, AAU, and AU. Focuses on fundamental AI research with applications in health, biotech, energy, and climate.
- **Relevance:** Denmark's flagship AI research center with health as a key application area.

---

## Diabetes & Clinical Research Tools

### steno-aarhus/osdc
- **URL:** https://github.com/steno-aarhus/osdc
- **Description:** Open-Source Diabetes Classifier (OSDC): an R package to classify diabetes status (type 1 and type 2) in Danish registers. Developed at Steno Diabetes Center Aarhus, validated for accuracy.
- **Relevance:** Directly relevant tool for classifying diabetes in Danish health registry data; exemplary open-source clinical research tool.

### steno-aarhus (Steno Diabetes Center Aarhus)
- **URL:** https://github.com/steno-aarhus
- **Description:** GitHub organization for Steno Diabetes Center Aarhus, containing research projects, data management tools, and documentation. Interdisciplinary group in machine learning and clinical prediction, affiliated with Aarhus University.
- **Relevance:** Active Danish health AI research group with multiple open-source projects.

### steno-aarhus/registers-project-database
- **URL:** https://github.com/steno-aarhus/registers-project-database
- **Description:** SDCA's project database on Denmark Statistics, documenting how to apply for and use Danish health register data.
- **Relevance:** Practical guide for working with Danish health registries; useful for anyone building AI on Danish register data.

### Seedcase Project
- **URL:** https://seedcase-project.org/ (developed at Steno Diabetes Center Aarhus)
- **Description:** Software for structuring, documenting, browsing, and sharing research data. Funded by a five-year Novo Nordisk Foundation grant. Developed at Steno Diabetes Center Aarhus and Aarhus University.
- **Relevance:** Research data management infrastructure relevant to health data projects in Denmark.

---

## Genomics & Epidemiology (Statens Serum Institut)

### ssi-dk (Statens Serum Institut)
- **URL:** https://github.com/ssi-dk
- **Description:** GitHub organization for Denmark's Statens Serum Institut with 121 repositories. SSI is responsible for infectious disease surveillance and epidemiology in Denmark.
- **Relevance:** Major Danish public health institution with extensive open-source bioinformatics and surveillance tools.

### ssi-dk/bifrost
- **URL:** https://github.com/ssi-dk/bifrost
- **Description:** Bacterial surveillance platform focused on quality control in Denmark. Includes components for genomic analysis, species identification, antimicrobial resistance detection, and serotyping.
- **Relevance:** National bacterial genomic surveillance infrastructure; relevant for infectious disease AI and public health.

### ssi-dk/bifrost_reporter
- **URL:** https://github.com/ssi-dk/bifrost_reporter
- **Description:** Bifrost reporter for External Quality Assessment (EQA), collecting and parsing genomic analysis results from Bifrost-generated YAML files.
- **Relevance:** Quality assurance tooling for genomic surveillance in Danish public health.

---

## Danish NLP & Language Technology

### alexandrainst/danlp
- **URL:** https://github.com/alexandrainst/danlp
- **Description:** DaNLP is a repository for Natural Language Processing resources for the Danish language. Provides datasets, models, and code examples for NLP tasks using spaCy, Transformers, Flair, and PyTorch. Licensed for commercial use. Developed by the Alexandra Institute.
- **Relevance:** Essential for any health AI project that needs to process Danish clinical text, patient notes, or health-related documents.

### alexandrainst/alexandra_ai
- **URL:** https://github.com/alexandrainst/alexandra_ai
- **Description:** A Python package for Danish data science from the Alexandra Institute.
- **Relevance:** General Danish data science toolkit applicable to health data analysis.

### alexandrainst/coral
- **URL:** https://github.com/alexandrainst/coral
- **Description:** Danish ASR (Automatic Speech Recognition) and TTS (Text-to-Speech) models from the CoRal project. Funded by the Innovation Fund.
- **Relevance:** Danish speech models relevant for voice-based health AI applications, patient interaction, and clinical dictation.

### fnielsen/awesome-danish
- **URL:** https://github.com/fnielsen/awesome-danish
- **Description:** A curated list of resources for Danish language technology, maintained by Finn Arup Nielsen (DTU). Includes corpora, language models (Danish BERT), word embeddings, and NLP tools.
- **Relevance:** Meta-resource for finding Danish language tools needed for health NLP applications.

### fnielsen/dasem
- **URL:** https://github.com/fnielsen/dasem
- **Description:** Danish Semantic analysis tools by Finn Arup Nielsen.
- **Relevance:** Semantic analysis capabilities for Danish text, applicable to health document understanding.

---

## Danish Statistics & Data Access

### rOpenGov/dkstat
- **URL:** https://github.com/rOpenGov/dkstat
- **Description:** R package providing API connection to the StatBank from Statistics Denmark. Functions to search tables, download metadata, and access actual data.
- **Relevance:** Access to Danish population statistics relevant for health research and epidemiological AI.

### mauran/API-Danmark
- **URL:** https://github.com/mauran/API-Danmark
- **Description:** A curated list of Danish APIs, including health-related APIs.
- **Relevance:** Directory of Danish APIs that may include health data endpoints.

---

## MitID & Authentication

### Hundter/MitID-ReverseEngineered
- **URL:** https://github.com/Hundter/MitID-ReverseEngineered
- **Description:** A human-understandable client implementation of the Danish MitID protocol. NOT a secure implementation -- intended for educational purposes only.
- **Relevance:** Reference for understanding the MitID authentication protocol used to access Danish health services (Sundhed.dk, e-journal, etc.). Official integration requires certified MitID brokers.

---

## eHealth Infrastructure Documentation

### docs.ehealth.sundhed.dk
- **URL:** https://docs.ehealth.sundhed.dk/
- **Description:** Official technical documentation for the Danish eHealth infrastructure. Includes OpenAPI 2.0 specifications for the SSL (Service, Support, and Logistics) APIs used in Danish telemedicine. Swagger files available for client code generation.
- **Relevance:** Primary API documentation for building applications on Danish eHealth infrastructure.

---

## Key Funding & Infrastructure Notes

- **Novo Nordisk Foundation** funds multiple projects including the Health Data Science Sandbox, Seedcase Project, Pioneer Centre for AI, and the Danish Centre for AI Innovation.
- **Gefion Supercomputer** (launched October 2024) is Denmark's first AI-ready supercomputer, funded by Novo Nordisk Foundation and NVIDIA, supporting health and life science AI research.
- **Computerome and UCloud** are the Danish supercomputing platforms hosting health data science workloads.
- **FUT (Faelles Udbredelse af Telemedicin)** is the national telemedicine platform built on FHIR, developed by Trifork and others.
- **MedCom** and **HL7 Denmark** maintain the interoperability standards used across the Danish health system.
- **4S Foundation** governs the OpenTele telemedicine platform with members including Danish regions, municipalities, and universities.
