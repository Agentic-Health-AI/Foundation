# Personal Health Data: Open-Source Projects Directory

> Research conducted 2026-02-26 for the Agentic Health project.
> Focus: tools that help individuals manage, analyze, or act on their personal health data.

---

## Table of Contents

1. [Apple Health Exporters & Analyzers](#apple-health-exporters--analyzers)
2. [Google Health Connect Tools](#google-health-connect-tools)
3. [Wearable Data - Multi-Platform](#wearable-data---multi-platform)
4. [Garmin Tools](#garmin-tools)
5. [Oura Ring Tools](#oura-ring-tools)
6. [Whoop Tools](#whoop-tools)
7. [Fitbit Tools](#fitbit-tools)
8. [Blood Work & Lab Result Analyzers](#blood-work--lab-result-analyzers)
9. [Personal Health Record (PHR) Systems](#personal-health-record-phr-systems)
10. [Self-Hosted Health Dashboards](#self-hosted-health-dashboards)
11. [AI-Powered Health Assistants & Agentic Tools](#ai-powered-health-assistants--agentic-tools)
12. [FHIR & Health Data Interoperability](#fhir--health-data-interoperability)
13. [Health Data Reference & Research Cross-Referencing](#health-data-reference--research-cross-referencing)
14. [Curated Lists & Meta-Resources](#curated-lists--meta-resources)

---

## Apple Health Exporters & Analyzers

### apple-health-mcp-server
- **GitHub:** https://github.com/the-momentum/apple-health-mcp-server
- **Description:** MCP server for querying Apple Health data with natural language. Imports and analyzes Apple Health XML exports using DuckDB. Enables LLM-powered natural language queries over health data.
- **Relevance:** Directly enables agentic AI workflows over Apple Health data via Model Context Protocol. High relevance for LLM-based health reasoning.

### Vital2AI
- **GitHub:** https://github.com/agalbourdin/vital2ai
- **Description:** Privacy-first, open-source iOS app to export Apple Health data into clean, AI-ready CSV files. Designed for use with Gemini, ChatGPT, Claude, and other LLMs.
- **Relevance:** Bridges the gap between Apple Health data silos and AI analysis. Directly supports agentic health workflows by producing AI-ready data.

### apple-health-exporter
- **GitHub:** https://github.com/mganjoo/apple-health-exporter
- **Description:** Python module to export Apple Health XML dump files to pandas DataFrames for analysis.
- **Relevance:** Foundation library for Python-based health data analysis pipelines.

### analyze-apple-health
- **GitHub:** https://github.com/entorb/analyze-apple-health
- **Description:** Python scripts for analyzing and visualizing Apple Health data exports.
- **Relevance:** Ready-made analysis and visualization scripts for Apple Health data.

### applehealth (krumjahn)
- **GitHub:** https://github.com/krumjahn/applehealth
- **Description:** Export Apple Health data and generate insights and visualizations using AI.
- **Relevance:** Combines export with AI-driven insight generation.

### apple-health (fedecalendino)
- **GitHub:** https://github.com/fedecalendino/apple-health
- **Description:** Python library to extract structured information from Apple Health exports.
- **Relevance:** Clean extraction library for building analysis pipelines.

### AppleHealthAnalysis
- **GitHub:** https://github.com/deepankardatta/AppleHealthAnalysis
- **Description:** R package to analyze exported Apple Health XML data.
- **Relevance:** R ecosystem support for Apple Health data analysis.

---

## Google Health Connect Tools

### HealthConnectExports
- **GitHub:** https://github.com/angeloanan/HealthConnectExports
- **Description:** Export and own your health data from Android Health Connect. Allows users to take control of their data.
- **Relevance:** Data sovereignty tool for Android users; enables downstream analysis.

### healthexport
- **GitHub:** https://github.com/teqxnology/healthexport
- **Description:** Export Health Connect data directly to Google Sheets or CSV. Supports date ranges and metrics including Activity, Body Measurements, Sleep, Nutrition, Cycle Tracking, and Vitals. Compatible with Strava, Garmin, Fitbit, Coros, Samsung, Polar, Withings, and Zepp/Amazfit.
- **Relevance:** Comprehensive Health Connect export tool with broad device compatibility.

### TaskerHealthConnect
- **GitHub:** https://github.com/RafhaanShah/TaskerHealthConnect
- **Description:** Android Health Connect plugin for Tasker, enabling automated health data workflows.
- **Relevance:** Enables automation pipelines for Android health data collection.

### react-native-health-connect
- **GitHub:** https://github.com/matinzd/react-native-health-connect
- **Description:** React Native library for Health Connect (Android). Allows building cross-platform health apps with Health Connect integration.
- **Relevance:** SDK for building custom health data apps on Android.

### HealthKMP
- **GitHub:** https://github.com/vitoksmile/HealthKMP
- **Description:** Kotlin Multiplatform wrapper for Apple HealthKit on iOS/watchOS and Google Health Connect on Android.
- **Relevance:** Cross-platform health data access layer, useful for building unified health apps.

---

## Wearable Data - Multi-Platform

### Open Wearables
- **GitHub:** https://github.com/the-momentum/open-wearables
- **Description:** Self-hosted platform to unify wearable health data through one AI-ready API. Supports Apple Health, Samsung Health Connect, Garmin, Polar, Suunto, and Whoop. Oura and Fitbit support planned. MIT licensed with zero per-user fees.
- **Relevance:** Core infrastructure for agentic health. Unified API across wearables enables building AI agents that reason over all wearable data in one place.

### wearablecompute
- **GitHub:** https://github.com/DigitalBiomarkerDiscoveryPipeline/wearablecompute
- **Description:** Open-source Python package with 50+ data and domain-driven features computable from wearables and mHealth sensor data. Part of the Digital Biomarker Discovery Pipeline.
- **Relevance:** Feature engineering library for wearable data. Enables extraction of clinically meaningful biomarkers from raw sensor data.

### quantified-flu
- **GitHub:** https://github.com/madprime/quantified-flu
- **Description:** Community citizen science project exploring whether wearables can warn when you are getting sick. Accepts Fitbit and Oura data and visualizes it around user-reported sickness dates.
- **Relevance:** Demonstrates cross-referencing wearable data with health events for actionable illness detection.

### Open_Health_Data_Analysis
- **GitHub:** https://github.com/chriotte/Open_Health_Data_Analysis
- **Description:** Gathers data from multiple sources (FitBit API, EliteHRV, etc.) for unified health data analysis.
- **Relevance:** Multi-source health data aggregation and analysis example.

---

## Garmin Tools

### GarminDB
- **GitHub:** https://github.com/tcgoetz/GarminDB
- **Description:** Download and parse data from Garmin Connect (or Garmin watch), FitBit CSV, and MS Health CSV files into SQLite databases. Analyze data with Jupyter notebooks. Installable via pip.
- **Relevance:** Mature, multi-format health data warehouse. Excellent foundation for personal health analytics.

### python-garminconnect
- **GitHub:** https://github.com/cyberjunky/python-garminconnect
- **Description:** Python 3 API wrapper for Garmin Connect. Access health metrics, activity data, device information, goals, and historical data.
- **Relevance:** Programmatic access to Garmin data for building custom analysis tools.

### garminexport
- **GitHub:** https://github.com/petergardfjall/garminexport
- **Description:** Library and tool for downloading/backing up Garmin Connect activities to local disk. Supports incremental backups.
- **Relevance:** Data ownership and backup tool for Garmin users.

### garmin-grafana
- **GitHub:** https://github.com/arpanghosh8453/garmin-grafana
- **Description:** Dockerized Python script to fetch Garmin health data and store in InfluxDB for long-term health trend visualization with Grafana.
- **Relevance:** Self-hosted health dashboard specifically for Garmin data. Good model for personal health monitoring.

### garmin-analysis
- **GitHub:** https://github.com/unboagable/garmin-analysis
- **Description:** Data pipeline and analytics toolkit for Garmin smartwatch data. Extracts, aggregates, and cleans health metrics in SQLite with tools for modeling, anomaly detection, and visualization.
- **Relevance:** Goes beyond dashboards into anomaly detection and modeling on personal health data.

---

## Oura Ring Tools

### oura-ring (hedgertronic)
- **GitHub:** https://github.com/hedgertronic/oura-ring
- **Description:** Tools for acquiring and analyzing Oura API data. OuraClient supports nine different API requests. Integrates with pandas for data analysis.
- **Relevance:** Comprehensive Oura data acquisition and analysis toolkit.

### python-ouraring
- **GitHub:** https://github.com/turing-complet/python-ouraring
- **Description:** Oura Ring API client for Python with pandas DataFrame conversion support.
- **Relevance:** Clean Python client for building Oura data pipelines.

### oura-ring (crystoll)
- **GitHub:** https://github.com/crystoll/oura-ring
- **Description:** Oura Ring data science exploration tooling. Includes example notebooks for loading, plotting, and visualizing correlations in Oura data.
- **Relevance:** Data science starter kit for Oura Ring analysis with example notebooks.

### oura-ring-api-etl
- **GitHub:** https://github.com/stevenschmatz/oura-ring-api-etl
- **Description:** ETL pipeline to load sleep, readiness, and activity data from the Oura Ring API into a personal data warehouse.
- **Relevance:** Personal data warehouse pattern for longitudinal Oura data tracking.

---

## Whoop Tools

### whoop-analyzer
- **GitHub:** https://github.com/patrickloeber/whoop-analyzer
- **Description:** Analyze Whoop workout data with Python. Extracts all workouts via Whoop API.
- **Relevance:** Python-based Whoop workout data analysis.

### whoop (hedgertronic)
- **GitHub:** https://github.com/hedgertronic/whoop
- **Description:** Tools for acquiring and analyzing Whoop API data. WhoopClient supports ten different API request types.
- **Relevance:** Comprehensive Whoop API client for data extraction and analysis.

### mywhoop
- **GitHub:** https://github.com/karl-cardenas-coding/mywhoop
- **Description:** Automatically download your Whoop data daily and save to local file or export to remote location. Written in Go.
- **Relevance:** Automated data ownership tool for Whoop. Supports continuous personal health data collection.

### whoops
- **GitHub:** https://github.com/kryoseu/whoops
- **Description:** Flask application that exports Whoop data into PostgreSQL or MySQL database.
- **Relevance:** Database-backed Whoop data storage for long-term analysis.

### go-whoop
- **GitHub:** https://github.com/marekq/go-whoop
- **Description:** Download sleep, workout, cycle, and recovery data using the Whoop API. Written in Go.
- **Relevance:** Lightweight Go-based Whoop data downloader.

---

## Fitbit Tools

### FitbitEDA
- **GitHub:** https://github.com/schbz/FitbitEDA
- **Description:** Jupyter Notebook for exploratory data analysis of Fitbit fitness tracker raw data archive files.
- **Relevance:** Ready-to-use notebook for Fitbit data exploration.

### fitbit-grafana
- **GitHub:** https://github.com/arpanghosh8453/fitbit-grafana
- **Description:** Script to fetch Fitbit data via API, store in local InfluxDB, and visualize with Grafana.
- **Relevance:** Self-hosted Fitbit health dashboard with Grafana visualization.

### fitbit (danecollins)
- **GitHub:** https://github.com/danecollins/fitbit
- **Description:** Tools to download all Fitbit data and perform analytics. Includes a simple local data cache with incremental updates.
- **Relevance:** Local-first Fitbit data management and analytics.

---

## Blood Work & Lab Result Analyzers

### BLOOD_TEST_ANALYSIS
- **GitHub:** https://github.com/cherry-1729-9090/BLOOD_TEST_ANALYSIS
- **Description:** Upload blood test reports in PDF format and analyze them using CrewAI framework with specialized AI agents. Provides comprehensive summaries and personalized health advice.
- **Relevance:** Highly relevant to agentic health. Uses multi-agent AI (CrewAI) to analyze blood work and produce actionable recommendations.

### Interpretation-blood-test-results
- **GitHub:** https://github.com/Mehranalam/Interpretation-blood-test-results
- **Description:** Open-source project for automated interpretation of blood test results. Takes inputs like WBC, RBC, etc. and provides interpretations.
- **Relevance:** Automated blood work interpretation engine.

### Blood-Test-Analyzer-Engine
- **GitHub:** https://github.com/sanatnayar/Blood-Test-Analyzer-Engine
- **Description:** Backend engine to process images of blood tests using OCR (Google Cloud Text Recognition API) and return measurements in digital format via Express/Node.js.
- **Relevance:** OCR-based digitization of paper blood test results.

### blood-analyzer
- **GitHub:** https://github.com/sebastianRytel/blood-analyzer
- **Description:** Parse blood test data from PDFs and save to database. Extracts blood parameters from analyzer machine output.
- **Relevance:** PDF parsing and database storage for blood test tracking over time.

### Doctalyzer
- **GitHub:** https://github.com/open-xyz/doctalyzer
- **Description:** Web application to help patients understand medical reports. Upload reports in various formats and receive plain-language interpretations.
- **Relevance:** Patient-facing medical report interpreter. Makes lab results accessible.

### awesome-biomarkers
- **GitHub:** https://github.com/markwk/awesome-biomarkers
- **Description:** Curated list of biomarkers, blood tests, and blood tracking resources. Open-source database and directory.
- **Relevance:** Reference resource for understanding biomarkers and blood tests. Useful knowledge base for agentic health systems.

---

## Personal Health Record (PHR) Systems

### Fasten Health
- **GitHub:** https://github.com/fastenhealth/fasten-onprem
- **Description:** Open-source, self-hosted personal/family electronic medical record manager. Aggregates data from multiple healthcare providers (insurance, hospitals, clinics, labs) into one dashboard. Supports FHIR-based data import.
- **Relevance:** Top-tier project for agentic health. Self-hosted, multi-provider health record aggregation. Could serve as the data backbone for AI health agents.

### OpenHealth
- **GitHub:** https://github.com/OpenHealthForAll/open-health
- **Description:** AI Health Assistant powered by your data. Combines personal health information with AI to provide private health guidance. Can run completely locally with Ollama for maximum privacy. Uses docling for document parsing.
- **Relevance:** Core agentic health project. Local-first AI health assistant that reasons over personal health data. Very high relevance.

### NLM Personal Health Record
- **GitHub:** https://github.com/lhncbc/phr
- **Description:** Web-based PHR system developed by the National Library of Medicine. Allows tracking health information for yourself and dependents. Uses national coding and terminology standards. Can bridge data exchange with EHR systems.
- **Relevance:** Government-backed PHR with interoperability standards. Foundation for standards-compliant personal health data management.

### MyGNUHealth
- **GitHub (mirror):** https://github.com/kant/mygnuhealth
- **Primary repo:** https://codeberg.org/gnuhealth/mygnuhealth
- **Description:** GNU Health Personal Health Record for desktop and mobile. Covers bio-psycho-social health spheres. Connects with health professionals for real-time data sharing. Built with Go/Fyne framework. Licensed GPLv3+. Part of GNU Solidario humanitarian project.
- **Relevance:** Holistic PHR covering biological, psychological, and social determinants of health. Unique multi-dimensional approach.

### OpenMed
- **GitHub:** https://github.com/ianrowan/OpenMed
- **Description:** Agentic personal medical assistant that understands your personal health data. Open-source platform to democratize health data analysis through AI-powered insights.
- **Relevance:** Directly agentic. Combines personal health data understanding with AI-powered analysis and recommendations.

---

## Self-Hosted Health Dashboards

### garmin-grafana
- **GitHub:** https://github.com/arpanghosh8453/garmin-grafana
- **Description:** Dockerized pipeline: Garmin data -> InfluxDB -> Grafana dashboards for long-term health trend visualization.
- **Relevance:** Model for self-hosted health monitoring with time-series visualization.

### fitbit-grafana
- **GitHub:** https://github.com/arpanghosh8453/fitbit-grafana
- **Description:** Fitbit data -> InfluxDB -> Grafana pipeline for personal health dashboards.
- **Relevance:** Self-hosted Fitbit health monitoring dashboard.

### Fasten Health (also listed under PHR)
- **GitHub:** https://github.com/fastenhealth/fasten-onprem
- **Description:** Also functions as a health dashboard, aggregating records from multiple providers into a unified view.
- **Relevance:** Dual-purpose: PHR and dashboard for consolidated medical record viewing.

---

## AI-Powered Health Assistants & Agentic Tools

### OpenHealth
- **GitHub:** https://github.com/OpenHealthForAll/open-health
- **Description:** AI health assistant that turns personal health data into actionable plans. Runs fully locally with Ollama. Uses docling for document parsing. Unbiased tool for long-term health management.
- **Relevance:** Flagship project for the agentic health concept. Local AI + personal data = actionable health guidance.

### OpenMed
- **GitHub:** https://github.com/ianrowan/OpenMed
- **Description:** Agentic personal medical assistant. Democratizes health data analysis through AI-powered insights over personal medical data.
- **Relevance:** Directly aligned with agentic health vision.

### apple-health-mcp-server
- **GitHub:** https://github.com/the-momentum/apple-health-mcp-server
- **Description:** MCP server enabling LLMs to query Apple Health data via natural language. DuckDB-powered backend.
- **Relevance:** Enables LLM agents to directly query and reason over Apple Health data.

### BLOOD_TEST_ANALYSIS
- **GitHub:** https://github.com/cherry-1729-9090/BLOOD_TEST_ANALYSIS
- **Description:** Multi-agent (CrewAI) blood test analysis with personalized health advice.
- **Relevance:** Multi-agent AI framework applied to personal health data interpretation.

### AI-Agents-for-Medical-Diagnostics
- **GitHub:** https://github.com/ahmadvh/AI-Agents-for-Medical-Diagnostics
- **Description:** Specialized LLM-based AI agents that analyze complex medical cases. Integrates insights from various medical professional perspectives for comprehensive assessments.
- **Relevance:** Multi-specialist agent architecture for medical case analysis.

### HealthFlow
- **GitHub:** https://github.com/yhzhu99/HealthFlow
- **Description:** Self-evolving AI agent with meta planning for autonomous healthcare research.
- **Relevance:** Advanced agentic architecture for healthcare. Meta-planning approach could be adapted for personal health reasoning.

### Awesome-AI-Agents-for-Healthcare
- **GitHub:** https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare
- **Description:** Curated list of latest advances on agentic AI and AI agents for healthcare.
- **Relevance:** Meta-resource tracking the entire agentic health AI space.

### Smart Health Monitor
- **GitHub:** https://github.com/elmalla/smart-health-monitor
- **Description:** AI-powered home monitoring for diabetic and heart patients. Uses medical-grade devices, predictive AI, and mobile app for vital sign tracking and health risk prediction.
- **Relevance:** Proactive health monitoring with predictive AI for chronic conditions.

---

## FHIR & Health Data Interoperability

### Metriport
- **GitHub:** https://github.com/metriport/metriport
- **Description:** Open-source universal API for healthcare data. Connects to health information networks. Supports FHIR R4, C-CDA, and PDF formats. YC S22 company.
- **Relevance:** Infrastructure layer for agentic health. Enables programmatic access to patient records across health networks.

### Fasten Health (FHIR support)
- **GitHub:** https://github.com/fastenhealth/fasten-onprem
- **Description:** Supports FHIR-based data import from healthcare providers. Self-hosted medical record aggregator.
- **Relevance:** FHIR-native personal health record aggregation.

### SMART on FHIR API Server
- **GitHub:** https://github.com/smart-on-fhir/api-server
- **Description:** Open-source FHIR server supporting patient- and clinician-facing apps.
- **Relevance:** Foundation for building FHIR-compliant personal health applications.

### awesome-FHIR
- **GitHub:** https://github.com/fhir-fuel/awesome-FHIR
- **Description:** Curated list of awesome FHIR software, libraries, tools, and resources.
- **Relevance:** Meta-resource for the FHIR ecosystem.

### FHIR EMR (beda-software)
- **GitHub:** https://github.com/beda-software/fhir-emr
- **Description:** Open-source EMR based on FHIR. Clean frontend for electronic medical records, customizable, leveraging HL7 FHIR as data model.
- **Relevance:** FHIR-native EMR that could interface with personal health tools.

### Microsoft FHIR Server
- **GitHub:** https://github.com/microsoft/fhir-server
- **Description:** Open-source implementation of the HL7 FHIR specification by Microsoft.
- **Relevance:** Enterprise-grade FHIR server that could back personal health data storage.

### Open Wearables (also listed above)
- **GitHub:** https://github.com/the-momentum/open-wearables
- **Description:** Unified API normalizing wearable data. Bridges wearable data into standardized formats.
- **Relevance:** Interoperability layer between wearable devices and health data systems.

---

## Health Data Reference & Research Cross-Referencing

### health-reference-data (Crowdsourcing Cures)
- **GitHub:** https://github.com/crowdsourcing-cures/health-reference-data
- **Description:** Health reference databases including foods, ingredients, symptoms, units of measurement, supplements, diagnostic codes, medications, and side-effects.
- **Relevance:** Knowledge base for contextualizing personal health data. Essential for agents that need to cross-reference user data with medical knowledge.

### crowdsourcing-cures-app
- **GitHub:** https://github.com/crowdsourcing-cures/crowdsourcing-cures-app
- **Description:** Chrome extension and web/Android/iOS app that aggregates and analyzes health data. Cross-references personal data with crowdsourced treatment outcomes.
- **Relevance:** Directly cross-references personal health data with aggregated research and treatment outcomes. Core agentic health concept.

### awesome-biomarkers
- **GitHub:** https://github.com/markwk/awesome-biomarkers
- **Description:** Curated database of biomarkers, blood tests, and tracking methods.
- **Relevance:** Reference data for interpreting blood work and biomarker trends.

### awesome-healthcare-datasets
- **GitHub:** https://github.com/geniusrise/awesome-healthcare-datasets
- **Description:** Healthcare and biomedical datasets for AI/ML. Includes MIMIC-III, NHANES, and other major clinical datasets.
- **Relevance:** Training and reference data for health AI systems.

### ClinicalDataSources
- **GitHub:** https://github.com/EpistasisLab/ClinicalDataSources
- **Description:** Open or easy-access clinical data sources for biomedical research.
- **Relevance:** Research data sources that agentic health tools could query for evidence-based recommendations.

---

## Curated Lists & Meta-Resources

### awesome-healthcare
- **GitHub:** https://github.com/kakoni/awesome-healthcare
- **Description:** Curated list of awesome open-source healthcare software, libraries, tools, and resources. Each link vetted for active maintenance and value. Covers EHR, imaging, ML/AI, data standards, and more. 2.9k+ stars.
- **Relevance:** Master index of the open-source healthcare ecosystem. Essential starting point for discovering new tools.

### awesome-quantified-self
- **GitHub:** https://github.com/woop/awesome-quantified-self
- **Description:** Websites, resources, devices, wearables, applications, and platforms for self-tracking.
- **Relevance:** Comprehensive quantified self ecosystem directory.

### Awesome-AI-Agents-for-Healthcare
- **GitHub:** https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare
- **Description:** Latest advances on agentic AI and AI agents for healthcare.
- **Relevance:** Directly tracks the agentic health AI space.

### awesome-FHIR
- **GitHub:** https://github.com/fhir-fuel/awesome-FHIR
- **Description:** Curated list of FHIR software, libraries, tools, and resources.
- **Relevance:** FHIR ecosystem directory.

---

## Summary: Top Projects for Agentic Health

The following projects are most directly relevant to building an agentic health ecosystem:

| Project | Why It Matters |
|---------|---------------|
| **OpenHealth** | Local-first AI health assistant over personal data |
| **OpenMed** | Agentic medical assistant for personal health data |
| **Fasten Health** | Self-hosted multi-provider health record aggregation |
| **Open Wearables** | Unified API across wearable devices, AI-ready |
| **apple-health-mcp-server** | LLM-queryable Apple Health data via MCP |
| **Metriport** | Universal healthcare data API (FHIR-native) |
| **BLOOD_TEST_ANALYSIS** | Multi-agent AI blood work analysis (CrewAI) |
| **crowdsourcing-cures-app** | Cross-references personal data with research outcomes |
| **health-reference-data** | Knowledge base for health data contextualization |
| **Awesome-AI-Agents-for-Healthcare** | Tracks the agentic health AI landscape |
| **wearablecompute** | Feature engineering for clinical biomarkers from wearables |
| **GarminDB** | Mature multi-format health data warehouse |
| **MyGNUHealth** | Holistic PHR covering bio-psycho-social health |
| **HealthFlow** | Self-evolving AI agent for healthcare research |
