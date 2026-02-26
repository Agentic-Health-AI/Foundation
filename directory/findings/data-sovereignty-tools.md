# Data Sovereignty Tools for Health

> Research compiled for the Agentic Health project.
> Last updated: 2026-02-26

Health data belongs to the individual. This document catalogs open-source tools, platforms, and frameworks that support patient-controlled, self-hosted, and privacy-preserving health data management.

---

## Table of Contents

1. [Self-Hosted Personal Health Records](#self-hosted-personal-health-records)
2. [Local-First and Offline Health Apps](#local-first-and-offline-health-apps)
3. [FHIR-Based Platforms and Personal Data Stores](#fhir-based-platforms-and-personal-data-stores)
4. [Open-Source EHR / EMR Systems](#open-source-ehr--emr-systems)
5. [Decentralized and Blockchain-Based Health Data](#decentralized-and-blockchain-based-health-data)
6. [Solid Pods and Linked Data for Health](#solid-pods-and-linked-data-for-health)
7. [Privacy-Preserving Health AI (Federated Learning and Differential Privacy)](#privacy-preserving-health-ai)
8. [Health Data Portability and Export Tools](#health-data-portability-and-export-tools)
9. [Consent Management for Health Data](#consent-management-for-health-data)
10. [Healthcare Data APIs and Interoperability](#healthcare-data-apis-and-interoperability)

---

## Self-Hosted Personal Health Records

### Fasten Health

- **URL:** https://github.com/fastenhealth/fasten-onprem
- **Website:** https://www.fastenhealth.com/
- **License:** Open Source
- **Description:** An open-source, self-hosted personal/family electronic medical record aggregator. Fasten connects to 25,000+ healthcare providers using FHIR and Smart-on-FHIR (OAuth2) to pull medical records into a single private store that never leaves the user's hands. Works offline and is extensible.
- **Relevance:** Core data sovereignty tool. Directly implements the principle that health data belongs to the individual. Self-hosted, offline-capable, provider-agnostic.

### Mere Medical

- **URL:** https://github.com/cfu288/mere-medical
- **License:** Open Source
- **Description:** An offline-first, self-hosted web app to aggregate and sync medical records from patient portals into one place. Built with a local-first architecture where core functionality runs on the user's device without any internet connection required.
- **Relevance:** Strong local-first design. Data stays on the user's device. Good complement to Fasten with its emphasis on offline operation.

### HealthBox

- **URL:** https://github.com/connervieira/HealthBox (community project)
- **License:** Open Source
- **Description:** A privacy-respecting, encrypted, open-source health data management system that provides a single place for applications, devices, and information sources to store health data.
- **Relevance:** Designed from the ground up for privacy. Acts as a local health data hub.

---

## Local-First and Offline Health Apps

### Tidy Health PHR

- **URL:** https://apps.apple.com/us/app/tidy-health-phr/id1463595216
- **Description:** Personal health record app where data stays on the user's devices. Works offline with no cloud dependency. No data mining or server-side storage.
- **Relevance:** Demonstrates the local-first model for personal health records on mobile. Data never leaves the device.

### Health Keeper

- **URL:** https://www.healthkeeper.app/
- **Description:** Completely offline health records and vitals tracking app. Optional Google Drive backup. No server infrastructure means no traditional HIPAA exposure surface.
- **Relevance:** Fully offline health record management. The absence of server infrastructure is itself a privacy feature.

### PACE

- **Description:** A secure fitness tracker for iOS and Android where fitness, health, geolocation data and preferences are end-to-end encrypted.
- **Relevance:** End-to-end encryption applied to health and fitness tracking data.

### FitoTrack

- **URL:** https://codeberg.org/jannis/FitoTrack
- **License:** Open Source (GPL)
- **Description:** Open-source, ad-free mobile app for logging and viewing workouts (running, cycling, hiking). No accounts, no cloud, no tracking.
- **Relevance:** Demonstrates fully sovereign fitness data with no external dependencies.

---

## FHIR-Based Platforms and Personal Data Stores

### Medplum

- **URL:** https://www.medplum.com/
- **GitHub:** https://github.com/medplum/medplum
- **License:** Apache 2.0
- **Description:** Open-source healthcare developer platform with a FHIR R4 API, SDK client libraries, React UI components, and server-side Bots for logic. Self-hostable, HIPAA and SOC2 compliant. Facilitates care for over 20 million patients.
- **Relevance:** The strongest open-source FHIR-native platform for building custom patient-controlled health apps. No vendor lock-in. Can serve as the backbone of a sovereign health data store.

### HAPI FHIR

- **URL:** https://hapifhir.io/
- **GitHub:** https://github.com/hapifhir/hapi-fhir
- **License:** Apache 2.0
- **Description:** Complete open-source implementation of the HL7 FHIR standard in Java. Can be self-hosted as a FHIR server (JPA Server). The reference implementation for many FHIR projects.
- **Relevance:** Foundational FHIR infrastructure. Can serve as the data layer for any self-hosted FHIR-based personal health record.

### Ottehr

- **URL:** https://www.ottehr.com/
- **License:** Open Source
- **Description:** An FHIR-native, open-source EHR designed for modern practices. Highly customizable and adaptable to specific clinical workflows.
- **Relevance:** Open-source EHR with full FHIR support. Useful as the clinical-facing side of a sovereign health data ecosystem.

### Beda FHIR-EMR

- **URL:** https://github.com/beda-software/fhir-emr
- **License:** Open Source
- **Description:** A clean, open-source frontend for electronic medical records built on the HL7 FHIR standard as its data model.
- **Relevance:** Provides a usable EMR interface on top of FHIR data stores. Can be paired with HAPI FHIR for a fully self-hosted stack.

---

## Open-Source EHR / EMR Systems

### OpenEMR

- **URL:** https://www.open-emr.org/
- **GitHub:** https://github.com/openemr/openemr
- **License:** GPL
- **Description:** The most widely deployed open-source EMR system globally. Supports 30+ languages, full clinical workflows, e-prescriptions, patient portal, and import/export of medical records.
- **Relevance:** Mature, battle-tested open-source EMR. Full data ownership and portability. Patient portal for direct access.

### OpenMRS

- **URL:** https://openmrs.org/
- **GitHub:** https://github.com/openmrs
- **License:** MPL 2.0
- **Description:** The world's leading open-source medical records platform, maintained by a global community. Originally designed for resource-limited settings but now used worldwide.
- **Relevance:** Global community-driven platform. Flexible data model. Strong focus on accessibility and local deployment.

### GNU Health

- **URL:** https://www.gnuhealth.org/
- **Source:** https://sourceforge.net/projects/gnu-health/
- **License:** GPL
- **Description:** Award-winning Hospital and Health Information System declared a Digital Public Good by the United Nations. Includes clinical workflow, patient records, laboratory management, medical stock management. "GNU Health in a Box" runs a full system on a single local machine with embedded Debian.
- **Relevance:** A Digital Public Good for health. The "in a Box" model is the ultimate self-hosted health system - no network needed. Used in public health systems across Argentina, India, Jamaica, Laos, Cameroon, and Suriname.

### Bahmni

- **URL:** https://www.bahmni.org/
- **License:** AGPL
- **Description:** Integrated clinical platform combining OpenMRS (patient records), OpenELIS (lab management), and Odoo (hospital operations). Developed by ThoughtWorks.
- **Relevance:** Full-stack hospital system from open-source components. Demonstrates how sovereign health data infrastructure can be built entirely from open tools.

### HospitalRun

- **URL:** https://hospitalrun.io/
- **GitHub:** https://github.com/HospitalRun
- **License:** GPL
- **Description:** Open-source software for developing-world hospitals. Offline-first design with CouchDB-based sync.
- **Relevance:** Offline-first hospital system. Built for environments with unreliable connectivity - the same design principles apply to data sovereignty.

---

## Decentralized and Blockchain-Based Health Data

### MedRec

- **URL:** https://medrec.media.mit.edu/
- **Description:** MIT-developed system for managing medical records using Ethereum smart contracts. Patients control their clinical EHR data and wearable data (e.g. Fitbit). Uses blockchain for access control, not data storage.
- **Relevance:** Academic proof-of-concept for blockchain-based patient-controlled health records. Demonstrates smart contract access control for medical data.

### MediLinker

- **URL:** https://www.frontiersin.org/articles/10.3389/fdata.2023.1146023
- **Description:** Blockchain-based decentralized health information management platform from UT Austin's Dell Medical School. Uses Hyperledger Indy for decentralized identifiers and Hyperledger Aries as middleware. Credentials stored in patient-controlled digital wallets.
- **Relevance:** Patient-centric decentralized identity for health. The wallet model puts credentials directly in patient hands.

### MediBloc

- **URL:** https://medibloc.com/
- **Description:** Decentralized healthcare information ecosystem on blockchain where medical records are kept securely and transferred by their rightful owners (the patients, not the hospitals).
- **Relevance:** Production blockchain platform explicitly designed around patient data ownership.

### IBM Medical-Blockchain (archived)

- **URL:** https://github.com/IBM/Medical-Blockchain
- **License:** Apache 2.0
- **Description:** Healthcare data management platform storing medical data off-chain with blockchain-based access control. Patients can upload, view, and manage access to their documents with full audit logs.
- **Relevance:** Reference architecture for off-chain health data with blockchain access control. Useful as a design pattern even though the project is archived.

---

## Solid Pods and Linked Data for Health

### Solid Project (by Tim Berners-Lee / Inrupt)

- **URL:** https://solidproject.org/
- **Company:** https://inrupt.com/
- **GitHub:** https://github.com/solid
- **Description:** Solid (Social Linked Data) is a specification that lets people store their personal data in "pods" (Personal Online Data Stores). Applications request access to data with user permission. Inrupt is the commercial company driving enterprise adoption.
- **Relevance:** The foundational architecture for user-controlled data on the web. Directly applicable to health data sovereignty.

### Solid and NHS (Greater Manchester pilot)

- **Description:** The NHS piloted Solid pods with Inrupt in Greater Manchester to create patient-centric health and care records. Doctors and caregivers access data from patients' pods with permission. Patients can also upload lifestyle app data alongside clinical data.
- **Relevance:** Real-world proof that Solid pods can work for health data at scale within a national health system. The most significant health data sovereignty pilot to date.

### Community Solid Server

- **URL:** https://github.com/CommunitySolidServer/CommunitySolidServer
- **License:** MIT
- **Description:** Open-source Solid server implementation that anyone can self-host. Provides the pod infrastructure for personal data storage.
- **Relevance:** Self-hostable Solid pod server. The building block for deploying personal health data pods.

---

## Privacy-Preserving Health AI

### OpenMined / PySyft / SyftBox

- **URL:** https://openmined.org/
- **GitHub:** https://github.com/OpenMined/PySyft
- **License:** Apache 2.0
- **Description:** Non-profit community building technology for secure computation across siloed data. PySyft extends PyTorch and TensorFlow with cryptographic and distributed technologies for privacy-preserving machine learning. SyftBox is a newer developer-friendly interface. PriMIA is their framework specifically for medical imaging.
- **Relevance:** The most important open-source project for privacy-preserving AI in health. Enables training models on hospital data without the data ever leaving the hospital. Directly supports data sovereignty by making data sharing unnecessary.

### NVIDIA FLARE (Federated Learning Application Runtime Environment)

- **URL:** https://nvidia.github.io/NVFlare/
- **GitHub:** https://github.com/NVIDIA/NVFlare
- **License:** Apache 2.0
- **Description:** Open-source, domain-agnostic SDK for federated learning. Supports PyTorch, TensorFlow, and NumPy. Includes homomorphic encryption and differential privacy. Used for medical imaging, genetic analysis, oncology, and COVID-19 research via NVIDIA Clara.
- **Relevance:** Production-grade federated learning for health AI. Allows multiple hospitals to collaboratively train AI models without sharing patient data.

### Vantage6

- **URL:** https://vantage6.ai/ / https://docs.vantage6.ai/
- **GitHub:** https://github.com/vantage6/vantage6
- **License:** Apache 2.0
- **Description:** Open-source privacy-preserving federated learning infrastructure. Originally developed for oncology in the Netherlands as the backbone of the Personal Health Train (PHT) initiative. Uses Docker containers for flexible algorithm deployment. Handles horizontally and vertically partitioned data.
- **Relevance:** Purpose-built for health data federation. The Personal Health Train concept ("algorithms travel to data, data stays put") is the operational definition of data sovereignty in research. Deployed in real clinical research networks.

### Flower (flwr)

- **URL:** https://flower.ai/
- **GitHub:** https://github.com/adap/flower
- **License:** Apache 2.0
- **Description:** A unified, framework-agnostic approach to federated learning, analytics, and evaluation. Supports any ML framework (TensorFlow, PyTorch, etc.) and any programming language.
- **Relevance:** General-purpose federated learning framework applicable to health AI. Its framework-agnostic design makes it highly flexible for different health data scenarios.

### PriMIA

- **URL:** https://g-k.ai/PriMIA/
- **Description:** Framework for end-to-end privacy-preserving machine learning on medical images, developed at Technical University of Munich, OpenMined, and Imperial College London.
- **Relevance:** Specifically designed for medical imaging AI with privacy guarantees. Built on PySyft.

---

## Health Data Portability and Export Tools

### Metriport

- **URL:** https://www.metriport.com/
- **GitHub:** https://github.com/metriport/metriport
- **License:** Open Source
- **Description:** Open-source universal API for healthcare data. Connects to the largest health information networks. Supports FHIR R4, C-CDA, and PDF formats. Helps digital health companies access and manage patient health data.
- **Relevance:** The open-source bridge between health information networks and patient-controlled applications. Enables data portability at scale.

### Health Auto Export

- **URL:** https://www.healthyapps.dev/
- **GitHub:** https://github.com/Lybron/health-auto-export
- **Description:** Tool to export Apple Health data. Supports viewing and analysis on Mac, or integration with Grafana. Covers health metrics (steps, heart rate, sleep, blood pressure) and workouts.
- **Relevance:** Practical tool for extracting data from Apple's walled garden into user-controlled systems.

### Open mHealth

- **URL:** https://www.openmhealth.org/
- **License:** Open Source
- **Description:** Open standard for mobile health data. Provides schemas and tools for formatting health data from various sources (including HealthKit) into standardized JSON.
- **Relevance:** Data standardization layer that enables portability. The Granola library helps convert HealthKit data to Open mHealth schemas.

### Open Wearables

- **Description:** Open-source, self-hosted platform for wearable data supporting Apple Health, Garmin, Polar, Whoop, Suunto and more. Includes an MCP server for connecting health data to LLM clients.
- **Relevance:** Aggregates wearable data into a self-hosted platform. The MCP server integration is forward-looking for agentic health AI.

### Apple Health MCP Server (by Momentum)

- **URL:** https://www.themomentum.ai/blog/apple-health-mcp-server-by-momentum
- **License:** Open Source
- **Description:** MCP (Model Context Protocol) server that enables AI agents to access and analyze Apple Health data locally.
- **Relevance:** Bridges Apple Health data into the agentic AI ecosystem while keeping data local.

---

## Consent Management for Health Data

### Consent2Share (C2S)

- **URL:** https://bhits.github.io/consent2share/
- **GitHub:** https://github.com/bhits/consent2share
- **Sponsor:** U.S. Substance Abuse and Mental Health Services Administration (SAMHSA)
- **License:** Open Source
- **Description:** Open-source consent management and data segmentation tool. Allows patients to determine which health information to share and not share with providers. Implements Data Segmentation for Privacy (DS4P) defined by ONC. Two components: Patient Consent Management (frontend) and Access Control Services (backend).
- **Relevance:** The reference open-source implementation for patient-controlled consent in health data exchange. Directly implements the principle that patients decide who sees what.

### Pryv.io

- **URL:** https://pryv.github.io/
- **License:** Open Source
- **Description:** Swiss-made personal data and consent management solution. Designed for building personal data and digital health apps with built-in consent workflows.
- **Relevance:** European privacy-by-design approach to health data consent. Swiss jurisdiction adds regulatory strength.

### MITRE Consent Management Software

- **URL:** https://www.mitre.org/our-impact/intellectual-property/consent-management-software
- **Description:** Infrastructure that allows patients to communicate privacy preferences, indicating situations under which they consent to share data. Integrates with health information exchanges.
- **Relevance:** From a trusted non-profit (MITRE). Designed for integration with existing health information exchanges.

### Blue Compass Consent Module

- **Description:** Open-source consent management module that allows participants to decide what health information to share with primary and specialty providers, particularly for substance use and mental health data. Integrates with HIEs and EHR systems.
- **Relevance:** Specialized consent management for sensitive behavioral health data.

### Databunker

- **URL:** https://databunker.org/
- **GitHub:** https://github.com/securitybunker/databunker
- **License:** MIT
- **Description:** Free, open-source project for personal data storage and consent management. Provides a secure vault for personal records with built-in consent tracking.
- **Relevance:** General-purpose but applicable to health. MIT license makes it easy to integrate into health data sovereignty stacks.

---

## Healthcare Data APIs and Interoperability

### Awesome Healthcare (curated list)

- **URL:** https://github.com/kakoni/awesome-healthcare
- **Description:** Comprehensive curated list of open-source healthcare software, libraries, tools, and resources maintained on GitHub.
- **Relevance:** Meta-resource for discovering additional tools in this space. Continuously updated by the community.

### HL7 FHIR Open Source Implementations

- **URL:** https://confluence.hl7.org/display/FHIR/Open+Source+Implementations
- **Description:** Official HL7 directory of open-source FHIR implementations across multiple programming languages and platforms.
- **Relevance:** The canonical list of open-source FHIR tools. Essential reference for building FHIR-based sovereign health data infrastructure.

### OpenEHR

- **URL:** https://openehr.org/
- **Description:** Open platform specification for health data. Provides vendor-neutral, standards-based architecture for electronic health records with a focus on clinical modeling.
- **Relevance:** Alternative to FHIR for structured health data. The archetype-based approach gives strong semantic interoperability.

---

## Summary: Recommended Stack for Data Sovereignty

For an individual seeking full health data sovereignty today, a practical stack might include:

| Layer | Tool | Purpose |
|-------|------|---------|
| **Personal Health Record** | Fasten Health or Mere Medical | Aggregate and store health records locally |
| **Data Standard** | HAPI FHIR (self-hosted) | FHIR-native data storage and API |
| **Data Import** | Metriport API | Pull records from health information networks |
| **Wearable Data** | Health Auto Export / Open Wearables | Export and aggregate wearable and sensor data |
| **Consent** | Consent2Share or Pryv.io | Patient-controlled consent management |
| **AI/Analytics** | PySyft / NVIDIA FLARE / Vantage6 | Privacy-preserving analysis without data sharing |
| **Identity** | Solid Pod (Community Solid Server) | Decentralized personal data store with linked data |

The key principle across all these tools: **data stays with the patient, algorithms travel to the data**.
