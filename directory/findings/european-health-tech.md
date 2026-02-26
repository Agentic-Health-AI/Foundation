# European & Nordic Open-Source Health Tech Projects

> Research compiled: 2026-02-26
> Focus: Open-source health technology projects from Europe, with emphasis on Scandinavia and the Nordics.

---

## Table of Contents

1. [European Health Data Space (EHDS) Infrastructure](#european-health-data-space-ehds-infrastructure)
2. [Nordic Cross-Border Health Data Initiatives](#nordic-cross-border-health-data-initiatives)
3. [FHIR Implementations for European Health Systems](#fhir-implementations-for-european-health-systems)
4. [OpenEHR Clinical Data Repositories](#openehr-clinical-data-repositories)
5. [European Biobank Open-Source Tools](#european-biobank-open-source-tools)
6. [OMOP / Observational Health Data (OHDSI/EHDEN)](#omop--observational-health-data-ohdsieden)
7. [Medical Imaging](#medical-imaging)
8. [Telemedicine Platforms](#telemedicine-platforms)
9. [Hospital & Health Information Systems](#hospital--health-information-systems)
10. [FHIR-Native EHR & EMR Platforms](#fhir-native-ehr--emr-platforms)
11. [Health Data Transformation & Compliance Tools](#health-data-transformation--compliance-tools)
12. [Health Insurance & Social Protection](#health-insurance--social-protection)
13. [Curated Lists & Meta-Resources](#curated-lists--meta-resources)
14. [Key Institutions & Ongoing Programs](#key-institutions--ongoing-programs)

---

## European Health Data Space (EHDS) Infrastructure

### HealthData@EU Central Platform
- **URL**: https://code.europa.eu/healthdataeu (source code) | https://acceptance.data.health.europa.eu/ (platform)
- **Description**: The European Commission's open-source central platform for the European Health Data Space. Facilitates secondary use of health data for research, innovation, policymaking, and public health. Hosts a Dataset Catalogue compiling metadata from EU Member States, research infrastructures, and third countries. Released under the European Union Public Licence 1.2.
- **Country**: EU (European Commission DG SANTE)
- **Relevance**: Core infrastructure of EHDS; the single most important EU-level open-source health data platform.

### Health DCAT-AP Specification
- **URL**: https://healthdcat-ap.github.io/
- **Description**: Data catalogue vocabulary and application profile standard (HealthDCAT-AP) that allows data holders to describe health datasets so they can be discovered through national catalogues and the HealthData@EU portal. Developed as part of the EHDS2 pilot.
- **Country**: EU
- **Relevance**: Core metadata standard for EHDS dataset discoverability.

### Hospitals On FHIR
- **URL**: https://www.hospitalsonfhir.eu/
- **Description**: A Community of Practice aimed at boosting interoperability maturity in healthcare organizations across Europe. Converges experts, industry, and EU-funded projects around HL7 FHIR as the route to interoperable healthcare aligned with the EHDS vision.
- **Country**: EU (multi-country)
- **Relevance**: Drives FHIR adoption in European hospitals to support both primary and secondary use of health data.

---

## Nordic Cross-Border Health Data Initiatives

### VALO (Value from Nordic Health Data)
- **URL**: https://www.sitra.fi/en/projects/value-from-nordic-health-data-valo/
- **Description**: Joint project between Denmark, Finland, Iceland, Norway, and Sweden (with Estonia and Lithuania as observers). Funded by the Nordic Council of Ministers and coordinated by Sitra (Finnish Innovation Fund) in partnership with THL (Finnish Institute for Health and Welfare). Aims to unlock the value of Nordic health data for research and innovation.
- **Country**: Nordic (DK, FI, IS, NO, SE)
- **Relevance**: High -- pan-Nordic health data collaboration, directly relevant to cross-border data sharing.

### Federated Health: A Nordic Federated Health Data Network
- **URL**: https://www.su.se/english/research/research-projects/federated-health-a-nordic-federated-health-data-network
- **Description**: Enables researchers from Norway, Sweden, Denmark, Finland, and Estonia to tap into a much larger virtual dataset without moving raw data across borders. Managed by Taridzo Chomutare from the Norwegian Centre for E-health Research.
- **Country**: Nordic/Baltic (NO, SE, DK, FI, EE)
- **Relevance**: Federated analysis approach preserves data sovereignty -- a model for cross-border health research.

### NORDeHEALTH
- **URL**: https://www.jmir.org/2024/1/e49084 (research output)
- **Description**: NordForsk-funded project (grant 100477) with research partners in Sweden, Norway, Finland, Estonia, and the US. Focuses on patient online record access, providing feedback to national authorities and guidelines for design, implementation, and evaluation of patient portals.
- **Country**: Nordic (SE, NO, FI, EE)
- **Relevance**: Patient portal research directly relevant to citizen access to health data.

### Nordic Interoperability Project
- **URL**: https://nordicinteroperability.com/
- **Description**: Project focused on improving health data interoperability across the Nordic countries, enabling seamless data exchange between national health systems.
- **Country**: Nordic
- **Relevance**: Foundation for Nordic health data exchange.

### TEHDAS2 (Second Joint Action Towards the European Health Data Space)
- **URL**: https://tehdas.eu/
- **Description**: Carried out by 29 European countries and coordinated by Sitra (Finland). Develops concrete guidelines and technical definitions for secondary use of health data. Creates technical specifications for secure data processing environments and common cybersecurity, interoperability, and traceability requirements. Funded by the EU4Health Programme, ending December 2026.
- **Country**: Finland (coordinator) + 28 EU countries
- **Relevance**: Defines the technical and governance framework for EHDS implementation.

---

## FHIR Implementations for European Health Systems

### Nordic FHIR Base Profiles
- **URL**: https://github.com/fhir-fi/nordic-base | https://build.fhir.org/ig/fhir-fi/nordic-base/
- **Description**: A collection of Nordic FHIR Base profiles in one implementation guide, covering Sweden, Norway, Finland, and Denmark. Harmonizes base profiles across the Nordic countries.
- **Country**: Nordic (FI, SE, NO, DK)
- **Relevance**: Foundation for Nordic FHIR interoperability.

### HL7 FHIR DK Core (Denmark)
- **URL**: https://hl7.dk/fhir/core/
- **Description**: Danish FHIR Core profiles that define adaptations of FHIR resources for use in Denmark. Harmonized with other Nordic base profiles.
- **Country**: Denmark
- **Relevance**: National FHIR standard for Denmark.

### HL7 Norway Base Profiles
- **URL**: https://github.com/HL7Norway/basisprofiler-r4
- **Description**: HL7 FHIR Base profiles for Norway (R4). Defines adaptations of FHIR resources for the Norwegian health system.
- **Country**: Norway
- **Relevance**: National FHIR standard for Norway.

### Finnish Base Profiles
- **URL**: https://hl7.fi/fhir/finnish-base-profiles/
- **Description**: Finnish FHIR base profiles harmonized with other Nordic country profiles. Maintained by HL7 Finland.
- **Country**: Finland
- **Relevance**: National FHIR standard for Finland.

### Nordic ePI (Electronic Product Information) FHIR IG
- **URL**: https://build.fhir.org/ig/felleskatalogen/nordic-epi-ig/
- **Description**: Nordic common standard for electronic product information (ePIL) represented as a FHIR implementation guide. Builds on HL7 Vulcan Accelerator's global ePI FHIR IG, compatible with EMA ePI pilot system.
- **Country**: Nordic
- **Relevance**: Standardizes medicine information across Nordic countries using FHIR.

### HL7 Europe Base Profiles
- **URL**: https://github.com/hl7-eu/base
- **Description**: European-level base profiles and common artefacts for FHIR. Proposes EU "Base" profiles as foundational definitions and EU "Core" profiles with key constraints for use across European implementation guides.
- **Country**: EU
- **Relevance**: Pan-European FHIR interoperability layer.

### HAPI FHIR
- **URL**: https://hapifhir.io/ | https://github.com/hapifhir/hapi-fhir
- **Description**: Complete open-source implementation of the HL7 FHIR standard for healthcare interoperability in Java. Licensed under Apache 2.0. Widely used across European health systems.
- **Country**: Canada (origin), but heavily used in Europe
- **Relevance**: Most widely adopted open-source FHIR server globally, foundational for many European implementations.

### Blaze FHIR Server
- **URL**: https://github.com/samply/blaze
- **Description**: A FHIR Server with an internal, fast CQL (Clinical Quality Language) Evaluation Engine. Implemented in Clojure, uses RocksDB as backend. Stable and widely used in the German Medical Informatics Initiative and biobanks across Europe.
- **Country**: Germany
- **Relevance**: High-performance FHIR server used in German Medical Informatics Initiative and European biobank infrastructure.

### MaLaC-HD (Mapping Language Compiler for Health Data)
- **URL**: https://gitlab.com/cdeHealth/malac-hd | https://pypi.org/project/malac-hd/
- **Description**: Open-source compiler that compiles FML (FHIR Mapping Language) code into Python. Achieves execution speeds nearly 100x faster than existing tools. Supports CDA-to-FHIR and FHIR R4-to-R5 transformations. Licensed under LGPL. Developed for EHDS preparation.
- **Country**: Austria
- **Relevance**: Critical tool for EHDS data format transformations (CDA to FHIR).

---

## OpenEHR Clinical Data Repositories

### EHRbase
- **URL**: https://github.com/ehrbase/ehrbase | https://www.ehrbase.org/
- **Description**: Open-source openEHR Clinical Data Repository providing a standard-based backend for interoperable clinical applications. Implements openEHR RM 1.1.0 and ADL 1.4. Developed by vitagroup (Germany) in collaboration with Hannover Medical School (MHH) and HiGHmed.
- **Country**: Germany
- **Relevance**: Leading open-source openEHR server; core infrastructure for openEHR-based health systems in Europe.

### EHRbase openEHR SDK
- **URL**: https://github.com/ehrbase/openEHR_SDK
- **Description**: SDK to facilitate the development of openEHR applications in Java. Companion tool for EHRbase.
- **Country**: Germany
- **Relevance**: Developer tooling for building openEHR applications.

### EHRServer
- **URL**: https://github.com/ppazos/cabolabs-ehrserver
- **Description**: Open-source, service-oriented openEHR clinical data repository designed by CaboLabs Health Informatics. Provides RESTful API for managing and sharing standardized clinical data.
- **Country**: Uruguay / International
- **Relevance**: Alternative open-source openEHR CDR used in European contexts.

### EtherCIS
- **URL**: https://ripple.foundation/ethercis/
- **Description**: An openEHR-based Clinical Data Repository built on SQL that exposes services via a REST API. Developed by the Ripple Foundation (UK).
- **Country**: United Kingdom
- **Relevance**: UK-origin openEHR CDR with European deployments.

---

## European Biobank Open-Source Tools

### BBMRI-ERIC (GitHub Organization)
- **URL**: https://github.com/BBMRI-ERIC
- **Description**: Biobanking and Biomolecular Resources - European Research Infrastructure Consortium. Maintains multiple open-source repositories for European biobank interoperability and data sharing.
- **Country**: EU (pan-European, HQ in Austria)
- **Relevance**: Central European research infrastructure for biobanking.

### BBMRI-ERIC Negotiator
- **URL**: https://github.com/BBMRI-ERIC/negotiator
- **Description**: Open-source access negotiation system for Research Infrastructures. Mediates structured negotiation for access to health data and biological samples within BBMRI-ERIC and other European research projects.
- **Country**: EU
- **Relevance**: Enables governed access to biobank samples and data across Europe.

### MIABIS (Minimum Information About BIobank data Sharing)
- **URL**: https://github.com/BBMRI-ERIC/miabis
- **Description**: Biobank-specific terminology enabling sharing of minimal biobank-related data across different database implementations. Defines the standard vocabulary for biobank metadata.
- **Country**: EU
- **Relevance**: Core metadata standard for European biobank interoperability.

### BiBBoX (Basic Infrastructure Building Box)
- **URL**: https://bibbox.bbmri-eric.eu/
- **Description**: Online platform providing 40+ different open-source software tools for biobanks free of charge. Especially useful for smaller and new biobanking operations.
- **Country**: EU (Austria-based)
- **Relevance**: Lowers the barrier to entry for biobanks adopting open-source tools.

### Samply (German Biobank Node / BBMRI-ERIC)
- **URL**: https://github.com/samply
- **Description**: Suite of open-source tools developed by the German Biobank Node in cooperation with BBMRI-ERIC. Includes the Sample Locator (cross-biobank search), Bridgehead architecture, Blaze FHIR Store, Focus/Beam communication layer, and transFAIR data integration tool. Sponsored by German Federal Ministry of Education and Research.
- **Country**: Germany
- **Relevance**: Core open-source infrastructure for federated biobank queries across Europe.

### Samply BBMRI-FHIR Implementation Guide
- **URL**: https://samply.github.io/bbmri-fhir-ig/ | https://github.com/samply/bbmri-fhir-ig
- **Description**: FHIR profiles for biobanking, defining how biobank data (collections, samples, diagnoses) is represented in FHIR format. Used across German Medical Informatics Initiative and European biobanks.
- **Country**: Germany / EU
- **Relevance**: Standard FHIR representation for biobank data in Europe.

### OpenSpecimen
- **URL**: https://github.com/krishagni/openspecimen
- **Description**: Open-source biobanking/biorepository management software. Manages biospecimen data across collection, consent, quality control, request, and distribution workflows.
- **Country**: India (origin), used globally including Europe
- **Relevance**: Widely adopted biobank management system in European research institutions.

---

## OMOP / Observational Health Data (OHDSI/EHDEN)

### OHDSI (Observational Health Data Sciences and Informatics)
- **URL**: https://github.com/OHDSI | https://www.ohdsi-europe.org/
- **Description**: International open-science community producing open-source tools for large-scale observational health data analytics using the OMOP Common Data Model. All tools are open source (R, Python, JavaScript). OHDSI Europe is a dedicated European chapter.
- **Country**: International (strong European chapter)
- **Relevance**: The OMOP CDM is becoming the standard for secondary use of health data in Europe, aligned with EHDS.

### EHDEN (European Health Data & Evidence Network)
- **URL**: https://github.com/EHDEN
- **Description**: IMI2-funded project building a large-scale, sustainable, federated network of European data sources standardized to the OMOP CDM. Provides open-source tools including CdmInspection (quality control for OMOP instances), CatalogueExport, and the EHDEN Academy (e-learning).
- **Country**: EU (multi-country consortium)
- **Relevance**: Builds the European OMOP CDM federated network; directly supports EHDS secondary use goals.

### EHDEN CdmInspection
- **URL**: https://github.com/EHDEN/CdmInspection
- **Description**: R package to support quality control inspection of an OMOP-CDM instance. Part of EHDEN's quality assurance pipeline.
- **Country**: EU
- **Relevance**: Essential quality control tool for European OMOP CDM deployments.

---

## Medical Imaging

### Orthanc
- **URL**: https://www.orthanc-server.com/ | https://github.com/jodogne/OrthancMirror
- **Description**: Free and open-source, lightweight DICOM server for medical imaging. Functions as a Vendor Neutral Archive (VNA). Runs on any hardware from Raspberry Pi to cloud infrastructure. RESTful API for integration. Developed at UCLouvain (Belgium). Licensed under GPLv3.
- **Country**: Belgium
- **Relevance**: Leading European open-source medical imaging server; widely deployed in hospitals and research.

---

## Telemedicine Platforms

### Servando
- **URL**: https://github.com/citiususc/servando
- **Description**: Open and distributed telemedicine platform based on Android. Developed by CITIUS (Centro de Investigacion en Tecnoloxias da Informacion) at the University of Santiago de Compostela. Allows development of generic telemedicine applications adaptable to specific diseases or patient characteristics.
- **Country**: Spain
- **Relevance**: European academic telemedicine platform with flexible architecture.

### MediPi
- **URL**: https://github.com/rprobinson/MediPi
- **Description**: Clinically led, community-based, open-platform telehealth system. Developed in partnership with Hertfordshire Community NHS Trust. Aims to make telehealth economically attractive.
- **Country**: United Kingdom
- **Relevance**: NHS-partnered open-source telehealth for community care.

---

## Hospital & Health Information Systems

### GNU Health
- **URL**: https://www.gnuhealth.org/ | https://github.com/msuarez/gnuhealth
- **Description**: Award-winning open-source Hospital and Health Information System covering Electronic Medical Records, Hospital Management, and Health Information Systems. Over 40 modules including primary care, surgery, pediatrics, and diagnostics. Declared a Digital Public Good by the United Nations. Official GNU package since 2011. Founded by Luis Falcon in Spain (Las Palmas).
- **Country**: Spain (Canary Islands)
- **Relevance**: Most comprehensive European-origin open-source hospital information system.

### openIMIS
- **URL**: https://openimis.org/ | https://github.com/openimis
- **Description**: Open-source software for administration of health financing and social protection schemes. Manages beneficiary, provider, and payer data. Impacts 36.6 million beneficiaries across 14 countries. Recognized as a Digital Public Good. Financed by Swiss SDC, German BMZ, and European Commission.
- **Country**: Switzerland / Germany / EU
- **Relevance**: European-funded open-source health insurance management used globally.

---

## FHIR-Native EHR & EMR Platforms

### Beda EMR (FHIR-EMR)
- **URL**: https://github.com/beda-software/fhir-emr | https://beda.software/emr
- **Description**: Open-source FHIR-native EMR powered by Aidbox FHIR Server. Features include Auth, User Management, fine-grained Access Control, telehealth, charting, and scheduling. CTO is an HL7 FHIR contributor.
- **Country**: Netherlands / International
- **Relevance**: Open-source FHIR-native EMR with strong European FHIR standards involvement.

### Ottehr
- **URL**: https://www.ottehr.com/
- **Description**: First FHIR-native, open-source EHR. Production-ready modular EHR with telehealth, charting, e-prescriptions, scheduling, and revenue cycle management modules.
- **Country**: USA (but relevant for European FHIR implementations)
- **Relevance**: Reference implementation for FHIR-native EHR architecture applicable to European deployments.

---

## Health Data Transformation & Compliance Tools

### Privado (GDPR Compliance)
- **URL**: https://www.privado.ai/ | https://github.com/Privado-Inc/privado
- **Description**: Open-source tool to automate compliance with privacy laws including GDPR and HIPAA. Identifies sensitive data in code, maps data flows, and detects compliance issues without executing code.
- **Country**: International (relevant for EU GDPR compliance)
- **Relevance**: Automates GDPR health data compliance checking in codebases.

### OpenDSR
- **URL**: https://opendsr.org/
- **Description**: Open-source framework for handling Data Subject Access Requests (DSARs) under GDPR. Provides a common API for companies to process privacy requests.
- **Country**: International / EU-focused
- **Relevance**: Supports GDPR compliance for health data subject access requests.

### LinuxForHealth / Project Alvearie
- **URL**: https://github.com/LinuxForHealth | https://github.com/Alvearie | https://alvearie.io/
- **Description**: IBM's open-source health data platform. Includes a FHIR Server (Java, Apache 2.0), de-identification capabilities supporting GDPR/HIPAA/CCPA, and health data pipeline components. LinuxForHealth provides a distributed processing network for healthcare transactions.
- **Country**: USA (IBM), but with GDPR support making it EU-relevant
- **Relevance**: Enterprise-grade open-source health data tools with explicit GDPR de-identification support.

---

## Health Insurance & Social Protection

### openIMIS
- *(See entry under Hospital & Health Information Systems above)*

---

## Curated Lists & Meta-Resources

### awesome-healthcare (by kakoni / Karri Niemela)
- **URL**: https://github.com/kakoni/awesome-healthcare
- **Description**: Curated list of awesome open-source healthcare software, libraries, tools, and resources. 3.6k+ stars. Maintained by Finnish developer Karri Niemela. Categories include EMR, imaging, FHIR, dental, lab systems, and hospital management.
- **Country**: Finland
- **Relevance**: Best single starting point for discovering open-source health tech projects.

### Awesome Digital Global Health
- **URL**: https://github.com/meleksomai/Awesome-Digital-Global-Health
- **Description**: Curated list of awesome Digital Global Health resources and software.
- **Country**: International
- **Relevance**: Broader global health perspective complementing European focus.

### awesome-healthcare-ai
- **URL**: https://github.com/medtorch/awesome-healthcare-ai
- **Description**: Curated list of awesome open-source healthcare tools, algorithms, datasets, and research papers focused on AI/ML in healthcare.
- **Country**: International
- **Relevance**: Reference for healthcare AI resources.

---

## Key Institutions & Ongoing Programs

### NordForsk
- **URL**: https://www.nordforsk.org/
- **Description**: Organization under the Nordic Council of Ministers that provides funding for Nordic research cooperation. Funds major health data projects including NORDeHEALTH and the Nordic Commons infrastructure for secure digital health data sharing.
- **Country**: Nordic

### Sitra (Finnish Innovation Fund)
- **URL**: https://www.sitra.fi/en/
- **Description**: Finnish innovation fund that coordinates VALO and TEHDAS2 projects. Key driver of Nordic and European health data policy.
- **Country**: Finland

### Nordic Innovation
- **URL**: https://www.nordicinnovation.org/
- **Description**: Nordic institution working to make it easier for businesses to innovate across borders. Supports health data innovation projects.
- **Country**: Nordic

### German Medical Informatics Initiative
- **URL**: Various (uses Samply, Blaze, EHRbase)
- **Description**: Major German federal initiative to improve the use of health data from patient care for research. Uses open-source tools (Blaze, Samply suite) and FHIR standards.
- **Country**: Germany

### Sundhed.dk (Denmark)
- **URL**: https://www.sundhed.dk/
- **Description**: Danish national e-health portal. Citizens can access health records, contact data, renew prescriptions, make appointments, and enter advance directives. One of the most advanced national patient portals in the world.
- **Country**: Denmark

### Kanta.fi (Finland)
- **URL**: https://www.kanta.fi/en/
- **Description**: Finnish national health data service. Serves as national contact point for cross-border health data exchange in the EU. Supports electronic prescriptions and patient records across European countries.
- **Country**: Finland

### 1177 Vardguiden (Sweden)
- **URL**: https://www.1177.se/
- **Description**: Swedish national health portal providing citizens with access to health information, online booking, and patient records.
- **Country**: Sweden

---

## Summary Statistics

| Category | Count |
|---|---|
| EHDS Infrastructure | 3 |
| Nordic Cross-Border Initiatives | 5 |
| FHIR Implementations | 10 |
| OpenEHR CDRs | 4 |
| Biobank Tools | 7 |
| OMOP/OHDSI Tools | 3 |
| Medical Imaging | 1 |
| Telemedicine | 2 |
| Hospital/HIS Systems | 2 |
| FHIR-Native EHR/EMR | 2 |
| Compliance & Transformation | 4 |
| Meta-Resources | 3 |
| Key Institutions | 7 |
| **Total entries** | **53** |

---

## Notes

- Many Nordic health data projects emphasize **federated approaches** that keep data within national borders while enabling cross-border research -- a pattern driven by GDPR requirements and national data sovereignty concerns.
- The **EHDS regulation** is accelerating open-source tooling development, particularly around FHIR, OMOP CDM, and secure processing environments.
- **OpenEHR** has strong adoption in Scandinavia (especially Sweden and Norway), with open-source CDR options like EHRbase serving as the backend.
- The **BBMRI-ERIC / Samply** ecosystem represents the most mature European open-source infrastructure for biobank data sharing.
- **FHIR harmonization** across Nordic countries is well advanced, with coordinated base profiles and a shared implementation guide.
