# Open Medical APIs, Databases, and Data Sources

> Research compiled for the Agentic Health project.
> Last updated: 2026-02-26

This document catalogs free and open APIs, databases, and data sources relevant to health AI agents. Each entry includes the resource name, URL, description, API details, and relevance to the project.

---

## Table of Contents

1. [Medical Research Literature APIs](#1-medical-research-literature-apis)
2. [Preprint Server APIs](#2-preprint-server-apis)
3. [Academic Search & Discovery](#3-academic-search--discovery)
4. [Clinical Trial Databases](#4-clinical-trial-databases)
5. [Drug & Pharmacology Databases](#5-drug--pharmacology-databases)
6. [Genomics & Variant Databases](#6-genomics--variant-databases)
7. [Disease-Gene Association Databases](#7-disease-gene-association-databases)
8. [Drug Target & Discovery Platforms](#8-drug-target--discovery-platforms)
9. [Medical Terminology & Ontology APIs](#9-medical-terminology--ontology-apis)
10. [Health Data Standards (FHIR/HL7)](#10-health-data-standards-fhirhl7)
11. [Rare Disease Databases](#11-rare-disease-databases)
12. [Global Health Statistics](#12-global-health-statistics)
13. [European Health Data Sources](#13-european-health-data-sources)
14. [Danish-Specific Health Data](#14-danish-specific-health-data)
15. [Protein & Molecular Databases](#15-protein--molecular-databases)
16. [Open-Source Wrappers & SDKs](#16-open-source-wrappers--sdks)

---

## 1. Medical Research Literature APIs

### PubMed E-utilities (Entrez)
- **URL**: https://www.ncbi.nlm.nih.gov/books/NBK25501/
- **API Base**: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/
- **Description**: NCBI's suite of server-side programs providing stable access to the Entrez query and database system, including PubMed (biomedical literature), PMC (full-text), and 35+ other databases.
- **API Details**: REST API. Key endpoints: ESearch (search), EFetch (retrieve records), ESummary (document summaries), ELink (related records), EInfo (database statistics). Returns XML or JSON. Rate limited to 3 req/sec without API key, 10 req/sec with key (free).
- **2026 Note**: PMC is migrating ESearch/EPost to updated versions. ESearch will be limited to first 10,000 records per query. PMC data distribution moving to Cloud Service (August 2026), replacing FTP.
- **Relevance**: **Critical** -- primary source for biomedical literature search and retrieval. Foundational for any health AI agent doing literature review.

### PubMed Central (PMC) OAI-PMH
- **URL**: https://pmc.ncbi.nlm.nih.gov/tools/oai/
- **Description**: Open Archives Initiative Protocol for Metadata Harvesting interface for PMC. Allows bulk retrieval of metadata and full-text XML for open access articles.
- **API Details**: OAI-PMH protocol. Returns Dublin Core or JATS XML. Full text XML available for open access subset.
- **Relevance**: **High** -- enables bulk harvesting of open access biomedical full-text articles for training or RAG pipelines.

### Europe PMC
- **URL**: https://europepmc.org/
- **API Docs**: https://europepmc.org/RestfulWebService
- **Description**: Free database of life science publications and preprints with over 33 million publications. Includes text-mined annotations (genes, proteins, diseases, chemicals) from full-text articles.
- **API Details**: RESTful API returning XML or JSON. Supports search, metadata retrieval, full-text access for OA articles, citation data, and text-mined annotations. Over 2 billion text-mined annotations available via dedicated Annotations API.
- **Relevance**: **High** -- European counterpart to PubMed with additional text-mining annotations. Valuable for entity extraction and knowledge graph construction.

---

## 2. Preprint Server APIs

### bioRxiv API
- **URL**: https://api.biorxiv.org/
- **API Docs**: https://api.biorxiv.org/pubs/help
- **Description**: Preprint server for biology. Now operated by openRxiv (non-profit, transferred from Cold Spring Harbor Laboratory in March 2025).
- **API Details**: REST API returning JSON or OAI-PMH XML. Results paginated at 100 articles per call with cursor-based iteration. Endpoints for content detail, published article detail, and usage statistics.
- **Relevance**: **High** -- access to cutting-edge biology research before peer review.

### medRxiv API
- **URL**: https://api.biorxiv.org/ (shared infrastructure with bioRxiv)
- **Description**: Preprint server for health sciences. Same API infrastructure as bioRxiv, also now under openRxiv.
- **API Details**: Same as bioRxiv API. Use `/medrxiv/` prefix in API calls instead of `/biorxiv/`.
- **Relevance**: **Critical** -- direct access to pre-publication medical research, essential for staying current with health research.

### ChemRxiv
- **URL**: https://chemrxiv.org/
- **Description**: Preprint server for chemistry and related areas, operated by the American Chemical Society.
- **API Details**: OpenAPI-compatible REST API with documentation available on the platform.
- **Relevance**: **Medium** -- relevant for drug chemistry, pharmacology, and biochemistry preprints.

### SSRN
- **URL**: https://www.ssrn.com/
- **Description**: Long-established preprint repository operated by Elsevier, covering social sciences, economics, health economics, and public health policy.
- **API Details**: Limited public API access. Primarily web-based access. Some data available through Elsevier APIs.
- **Relevance**: **Low-Medium** -- useful for health economics and public health policy papers.

---

## 3. Academic Search & Discovery

### Semantic Scholar
- **URL**: https://www.semanticscholar.org/
- **API Docs**: https://api.semanticscholar.org/api-docs/
- **Description**: AI-powered academic search engine by Allen Institute for AI, indexing over 214 million papers across all fields including biomedical literature.
- **API Details**: REST API. Most endpoints publicly available without authentication (rate-limited to 1000 req/sec shared among unauthenticated users). Higher limits with free API key. Endpoints for paper search, paper details, author info, citation networks, recommendations. Returns JSON.
- **Relevance**: **High** -- excellent for AI-powered literature discovery, citation analysis, and finding related medical research.

### OpenAlex
- **URL**: https://openalex.org/
- **API Docs**: https://docs.openalex.org/
- **Description**: Free and open catalog of the global research system, replacing Microsoft Academic Graph. Indexes works, authors, institutions, venues, and concepts.
- **API Details**: REST API, no authentication required. Returns JSON. Covers 250M+ works. Supports filtering, grouping, and complex queries.
- **Relevance**: **High** -- open alternative to proprietary academic databases, useful for bibliometric analysis of health research.

---

## 4. Clinical Trial Databases

### ClinicalTrials.gov API v2
- **URL**: https://clinicaltrials.gov/
- **API Docs**: https://clinicaltrials.gov/data-api/api
- **Description**: U.S. NLM registry and results database of clinical studies worldwide. The primary global clinical trials registry.
- **API Details**: REST API v2 (replaced classic API in June 2024). OpenAPI 3.0 specification. Returns JSON and CSV. Supports study search, study details, field values enumeration, and data statistics. Uses ISO 8601 dates. Fields use enumerated values for standardization.
- **Relevance**: **Critical** -- essential for any health AI agent that needs to find, analyze, or monitor clinical trials.

### WHO ICTRP (International Clinical Trials Registry Platform)
- **URL**: https://www.who.int/tools/clinical-trials-registry-platform
- **Search Portal**: https://trialsearch.who.int
- **Description**: WHO platform providing a single point of access to clinical trial information from registries worldwide. Aggregates data from multiple national and regional registries.
- **API Details**: Search portal available; data download options exist. Limited formal API -- primarily web search interface and periodic data exports.
- **Relevance**: **High** -- global aggregator especially useful for trials not registered on ClinicalTrials.gov.

### EU Clinical Trials Information System (CTIS)
- **URL**: https://euclinicaltrials.eu/
- **Description**: Supports clinical trials in the EU/EEA. Designated as a WHO primary registry. Replaced the EU Clinical Trials Register (EudraCT).
- **API Details**: Public search interface. Data available for download. API access expanding.
- **Relevance**: **High** -- primary source for European clinical trials data.

### OpenTrials
- **URL**: https://opentrials.net/
- **GitHub**: https://github.com/opentrials/
- **Description**: Open database aggregating clinical trial data from ClinicalTrials.gov, WHO ICTRP, EU CTR, and other sources.
- **API Details**: Open API with programmatic access to aggregated trial data.
- **Relevance**: **Medium** -- useful as a unified interface across multiple trial registries. (Note: project activity may be limited.)

---

## 5. Drug & Pharmacology Databases

### OpenFDA
- **URL**: https://open.fda.gov/
- **API Docs**: https://open.fda.gov/apis/
- **GitHub**: https://github.com/FDA/openfda
- **Description**: FDA open data platform providing access to drug adverse events (FAERS), product labeling, NDC directory, device recalls, food enforcement, and more.
- **API Details**: Elasticsearch-based REST API. No authentication required. Key drug endpoints: `/drug/event.json` (adverse events), `/drug/label.json` (labeling), `/drug/ndc.json` (NDC directory). Also covers devices, food, animal/vet, tobacco. Max 1000 records per call. Returns JSON. Supports search, count, and filtering.
- **Relevance**: **Critical** -- primary open source for FDA regulatory data including adverse events, drug labels, and recalls.

### RxNorm
- **URL**: https://www.nlm.nih.gov/research/umls/rxnorm/
- **API Docs**: https://lhncbc.nlm.nih.gov/RxNav/APIs/index.html
- **Description**: NLM's standardized nomenclature for clinical drugs and drug delivery devices. Provides normalized names and unique identifiers (RXCUIs) for medicines.
- **API Details**: REST APIs via RxNav. Endpoints include RxNorm API (drug name lookups, relationships), RxClass (drug classes), MED-RT (clinical drug properties), RxTerms (clinical terms). Returns JSON or XML. Free, no authentication.
- **Relevance**: **Critical** -- standard for drug name normalization and interoperability. Essential for mapping between different drug naming systems.

### DailyMed
- **URL**: https://dailymed.nlm.nih.gov/
- **API Docs**: https://dailymed.nlm.nih.gov/dailymed/app-support-web-services.cfm
- **Description**: NLM database providing the most recent drug labeling (SPL - Structured Product Labeling) submitted to the FDA. Covers prescription, OTC, medical gases, devices, dietary supplements.
- **API Details**: REST API v2. Query by drug name, application number, DEA schedule, boxed warning status, etc. Returns SPL data in ZIP or PDF. Bulk download available (daily, weekly, monthly updates or full releases).
- **Relevance**: **High** -- authoritative source for current FDA-approved drug labeling information.

### DrugBank
- **URL**: https://go.drugbank.com/
- **API Docs**: https://docs.drugbank.com/
- **Description**: Comprehensive drug database with detailed drug-drug interactions, side effects, targets, pharmacology, and chemical data.
- **API Details**: Clinical API available (commercial). Free academic access to downloadable data (requires application). XML data dumps available for research use.
- **Relevance**: **High** -- one of the most comprehensive drug databases. Free academic access available but commercial API requires subscription.

---

## 6. Genomics & Variant Databases

### ClinVar
- **URL**: https://www.ncbi.nlm.nih.gov/clinvar/
- **API Docs**: https://www.ncbi.nlm.nih.gov/clinvar/docs/api_http/
- **Description**: NCBI public archive of reports on relationships between human variations and phenotypes, with supporting evidence. Critical for clinical genetics.
- **API Details**: Entrez E-utilities for search/retrieval. Dedicated HTTP Submission API. FTP downloads available. VCF files available for bulk data.
- **Relevance**: **Critical** -- essential for any genetics/genomics health AI agent. Maps variants to clinical significance.

### gnomAD (Genome Aggregation Database)
- **URL**: https://gnomad.broadinstitute.org/
- **Description**: Aggregates exome and genome sequencing data from large-scale projects. Provides allele frequencies and variant annotations for the scientific community.
- **API Details**: GraphQL API for programmatic queries. Data also available on AWS Registry of Open Data, Azure Open Datasets, and Google Cloud. No restrictions on use of summary data.
- **Relevance**: **High** -- essential reference for population-level variant frequency data in genetics research.

### OMIM (Online Mendelian Inheritance in Man)
- **URL**: https://www.omim.org/
- **API Docs**: https://www.omim.org/api
- **Description**: Comprehensive compendium of human genes and genetic phenotypes, updated daily. Covers all known Mendelian disorders and over 15,000 genes.
- **API Details**: REST API over HTTPS. Requires API key (free for academic/research use, application required). Returns structured data on genes, phenotypes, and genotype-phenotype relationships.
- **Relevance**: **High** -- authoritative resource for genetic disorders. API access requires application but is free for research.

---

## 7. Disease-Gene Association Databases

### DisGeNET
- **URL**: https://disgenet.com/
- **Description**: One of the largest repositories of human gene-disease associations (GDAs) and variant-disease associations (VDAs). Contains 4.75M+ VDAs across 19,000+ diseases.
- **API Details**: REST API for programmatic retrieval. Also available as Linked Open Data with SPARQL endpoint. Cytoscape plugin available. Free for academic use; commercial license for industry.
- **Relevance**: **High** -- valuable for understanding genetic underpinnings of diseases and for drug repurposing research.

---

## 8. Drug Target & Discovery Platforms

### Open Targets Platform
- **URL**: https://platform.opentargets.org/
- **Description**: Data integration platform for systematic drug target identification and prioritization. Integrates GWAS, rare disease genetics, somatic mutations, known drugs, expression data, animal models, and pathway data from 22 sources.
- **API Details**: GraphQL API. Data available through API, web UI, and bulk downloads. Pipeline and infrastructure are open-source. Version 2.0 merged the separate Genetics portal into the main Platform API.
- **Relevance**: **High** -- powerful resource for drug target validation and disease-target association evidence.

---

## 9. Medical Terminology & Ontology APIs

### UMLS Terminology Services
- **URL**: https://uts.nlm.nih.gov/
- **API Docs**: https://documentation.uts.nlm.nih.gov/
- **Description**: NLM's Unified Medical Language System. Provides access to SNOMED CT, ICD-10, MeSH, RxNorm, LOINC, and 200+ other vocabularies and their mappings.
- **API Details**: REST API. Requires free UMLS license (registration required). Supports concept lookup, crosswalks between vocabularies, semantic network queries, and content views.
- **Relevance**: **Critical** -- the master resource for medical terminology mapping and interoperability. Required for standardizing clinical concepts.

### MeSH (Medical Subject Headings)
- **URL**: https://www.nlm.nih.gov/mesh/meshhome.html
- **RDF/API**: https://id.nlm.nih.gov/mesh/
- **Lookup Service**: https://id.nlm.nih.gov/mesh/lookup
- **Description**: NLM's controlled vocabulary for indexing and searching biomedical literature. Hierarchically organized with 30,000+ descriptors.
- **API Details**: SPARQL endpoint for RDF queries. RESTful lookup service returning JSON. Supports autocomplete, URI resolution, qualifier lookups. Downloadable in RDF N-Triples format. No authentication required.
- **Relevance**: **High** -- essential for standardized literature search and biomedical concept hierarchies.

### SNOMED CT
- **URL**: https://www.snomed.org/
- **NLM Access**: https://www.nlm.nih.gov/healthit/snomedct/index.html
- **Description**: Comprehensive clinical terminology system with 350,000+ concepts covering clinical findings, procedures, body structures, substances, and more.
- **API Details**: Accessible via UMLS Terminology Services API (requires UMLS license). SNOMED CT Browser available. SNOMED CT to ICD-10-CM mapping reference sets available (126,000+ mapped concepts). Free use in IHTSDO member countries (including US and Denmark) and for qualifying research projects.
- **Relevance**: **Critical** -- the international standard for clinical terminology. Essential for any clinical NLP or health data standardization.

### ICD-10 / ICD-11
- **URL**: https://icd.who.int/
- **API**: https://icd.who.int/icdapi
- **Description**: WHO's International Classification of Diseases. ICD-11 is the latest version with a modern API. Used globally for mortality/morbidity coding.
- **API Details**: REST API for ICD-11 (requires free registration). Supports coding tool, search, entity lookup, and linearization queries. ICD-10 data accessible via UMLS or WHO data tools.
- **Relevance**: **Critical** -- universal disease classification system. Required for any agent working with diagnostic codes.

---

## 10. Health Data Standards (FHIR/HL7)

### HAPI FHIR (Open Source FHIR Server)
- **URL**: https://hapifhir.io/
- **GitHub**: https://github.com/hapifhir/hapi-fhir
- **Description**: Complete open-source implementation of HL7 FHIR in Java. Apache 2.0 license. The most widely used open-source FHIR server.
- **API Details**: Full FHIR R4/R5 REST API. Supports all resource types, CRUD operations, search, batch/transaction, subscriptions. Can be deployed as a standalone server or embedded library.
- **Relevance**: **Critical** -- essential for building health AI agents that interact with clinical systems via FHIR.

### HL7 FHIR Public Test Servers
- **URL**: https://confluence.hl7.org/display/FHIR/Public+Test+Servers
- **Description**: Directory of publicly available FHIR servers for testing and development.
- **Key Servers**:
  - HAPI FHIR Test Server: https://hapi.fhir.org/
  - Health Samurai (Aidbox): Free tier available
  - AEGIS WildFHIR: R4 v4.0.1 reference test server
- **Relevance**: **High** -- test environments for developing FHIR-based health AI integrations.

### Microsoft FHIR Server
- **URL**: https://github.com/microsoft/fhir-server
- **Description**: Open-source FHIR server implementation for Azure and local deployment.
- **API Details**: Full FHIR R4 REST API. Designed for cloud deployment on Azure but can run locally.
- **Relevance**: **Medium** -- alternative FHIR server option for cloud-based deployments.

---

## 11. Rare Disease Databases

### Orphanet / Orphadata API
- **URL**: https://www.orpha.net/
- **API**: https://api.orphacode.org/
- **GitHub**: https://github.com/Orphanet/API_Orphadata
- **Data Portal**: https://www.orphadata.com/
- **Description**: The portal for rare diseases and orphan drugs. Provides structured data on rare disease classifications, gene associations, phenotypes, epidemiology, and natural history.
- **API Details**: REST API powered by Elasticsearch and Python Flask. Monthly data updates. Free access to: rare disease alignments with terminologies, clinical classifications, phenotype associations, gene associations, linearizations, epidemiology data, and natural history data. Returns JSON.
- **Relevance**: **High** -- the primary international resource for rare disease information. Essential for any rare disease-focused health AI.

### GARD (Genetic and Rare Diseases Information Center)
- **URL**: https://rarediseases.info.nih.gov/
- **Description**: NIH resource providing information about rare diseases. Data is partially curated manually and partially extracted programmatically from Orphanet.
- **API Details**: No dedicated public REST API. Data integrated into knowledge graphs. Linked data available through research publications.
- **Relevance**: **Medium** -- useful NIH resource but limited programmatic access. Orphanet is preferred for API-based access.

---

## 12. Global Health Statistics

### WHO Global Health Observatory (GHO) OData API
- **URL**: https://www.who.int/data/gho
- **API Docs**: https://www.who.int/data/gho/info/gho-odata-api
- **API Base**: https://ghoapi.azureedge.net/api/
- **Description**: WHO's gateway to health statistics for 194 member states. Over 1,000 indicators covering mortality, communicable diseases, NCDs, health systems, environmental health, and more.
- **API Details**: OData (Open Data Protocol) REST API. Returns JSON. Supports filtering by indicator, country, year, and other dimensions. No authentication required.
- **Note**: The current OData API is scheduled for deprecation and replacement with a new implementation (originally planned for late 2025).
- **Relevance**: **High** -- essential for population-level health data and global health monitoring.

---

## 13. European Health Data Sources

### European Medicines Agency (EMA) Data
- **URL**: https://www.ema.europa.eu/
- **Data Downloads**: https://www.ema.europa.eu/en/medicines/download-medicine-data
- **Clinical Data**: https://clinicaldata.ema.europa.eu/
- **Description**: EU regulatory authority for medicines. Publishes open data on authorized medicines (EPARs), clinical data from marketing applications, and regulatory decisions.
- **API Details**: Website data available in JSON for automated extraction. Tabular data downloads updated overnight. Clinical data publication portal provides access to clinical study reports. Third-party API wrappers exist (e.g., api.store).
- **Relevance**: **High** -- authoritative European drug regulatory data. EMA is the first regulatory authority to provide broad public access to clinical data.

### ECDC (European Centre for Disease Prevention and Control)
- **URL**: https://www.ecdc.europa.eu/
- **Surveillance Atlas**: https://atlas.ecdc.europa.eu/
- **Description**: EU agency for communicable disease surveillance. Provides data on infectious disease incidence, antimicrobial resistance, vaccination coverage, and outbreak reports across Europe.
- **API Details**: Surveillance Atlas provides interactive data access. Data downloads available. Involved in European Health Data Space (EHDS) pilot projects.
- **Relevance**: **High** -- essential for European infectious disease surveillance and public health data.

### DARWIN EU (Data Analysis and Real-World Interrogation Network)
- **URL**: https://www.darwin-eu.org/
- **Description**: EMA's distributed network for generating real-world evidence to support regulatory decision-making. Connects to multiple European health databases.
- **API Details**: Not a public API per se, but a federated data network. Access coordinated through EMA for regulatory purposes.
- **Relevance**: **Medium** -- important for understanding real-world evidence infrastructure in Europe.

### European Health Data Space (EHDS)
- **URL**: https://health.ec.europa.eu/ehealth-digital-health-and-care/european-health-data-space_en
- **Description**: EU framework for cross-border health data sharing for healthcare, research, innovation, and policy-making. Sets up unified health data infrastructure.
- **API Details**: Framework under development. Will standardize access to health data across EU member states.
- **Relevance**: **Medium-High** -- future infrastructure that will shape European health data access.

---

## 14. Danish-Specific Health Data

### Sundhedsdatastyrelsen (Danish Health Data Authority)
- **URL**: https://sundhedsdatastyrelsen.dk/ (Danish) / https://english.sundhedsdatastyrelsen.dk/ (English)
- **Description**: Manages national health registers containing data on the entire Danish population and healthcare system. The National Patient Register contains 40+ years of hospital data.
- **Data Access**: Research access available through the Secure Research Platform (Forskermaskinen) via application to Research Services. Not a public API -- requires formal data access application.
- **Key Registers**: National Patient Register, National Prescription Registry, Cause of Death Register, Cancer Register, Danish National Birth Cohort, and many others.
- **Note**: From January 2026, sundhed.dk, the Danish Health Data Authority, and MedCom are being consolidated into "Preparatory Digital Health Denmark" (Digitalt Sundhedsdanmark).
- **Relevance**: **High** for Danish context -- world-class population health registers, but access is restricted to approved research projects.

### sundhed.dk
- **URL**: https://www.sundhed.dk/
- **Description**: Denmark's national health portal providing citizens access to their health records, prescriptions, and healthcare services.
- **API Details**: Internal APIs serve the portal; no public research API.
- **Note**: Being consolidated into Digital Health Denmark from 2026.
- **Relevance**: **Medium** -- important Danish health infrastructure but no open API for external use.

### Denmark and SNOMED CT
- **URL**: https://www.snomed.org/members/denmark
- **Description**: Denmark is a member of SNOMED International, meaning SNOMED CT is freely available for use in Denmark.
- **Relevance**: **High** -- SNOMED CT can be freely used in Danish health AI applications.

---

## 15. Protein & Molecular Databases

### UniProt
- **URL**: https://www.uniprot.org/
- **API Docs**: https://www.uniprot.org/api-documentation
- **Description**: Universal Protein Knowledgebase -- comprehensive resource for protein sequence and functional information. Covers UniProtKB, UniRef, UniParc, Proteomes, and more.
- **API Details**: REST API, free and open, no authentication required. Averages 303 million requests/month. Supports structured queries with logical operators, field selection, bulk ID mapping (up to 100K IDs per job). Returns JSON, TSV, FASTA, and other formats.
- **Relevance**: **High** -- essential for any health AI agent working with protein/molecular data, drug targets, or genomics.

### Ensembl REST API
- **URL**: https://rest.ensembl.org/
- **Description**: Genome browser and annotation system. Provides gene, variant, regulatory, and comparative genomics data for vertebrate genomes.
- **API Details**: REST API with 100+ endpoints. No authentication required. Supports variant effect prediction, gene lookup, sequence retrieval, cross-references, and more.
- **Relevance**: **High** -- key resource for genome annotation and variant interpretation.

---

## 16. Open-Source Wrappers & SDKs

### Python Libraries

| Library | Target API | PyPI | Description |
|---------|-----------|------|-------------|
| **Biopython (Bio.Entrez)** | PubMed/NCBI Entrez | `biopython` | Mature library for NCBI E-utilities. Handles rate limiting, XML parsing, all E-utility functions. |
| **Entrezpy** | NCBI Entrez | `entrezpy` | Pure Python 3 library for Entrez. Automates complex queries, supports caching. No external dependencies. |
| **easy-entrez** | NCBI Entrez | `easy-entrez` | Simplified Python wrapper for Entrez E-utilities with clean API. |
| **paperscraper** | PubMed, arXiv, medRxiv, bioRxiv, ChemRxiv | `paperscraper` | Scrapes publications and metadata from multiple preprint/publication sources. |
| **PyMedTermino** | SNOMED CT, ICD-10, MedDRA, UMLS | `PyMedTermino` | Python module for accessing major medical terminologies. |
| **semanticscholar** | Semantic Scholar | `semanticscholar` | Python wrapper for Semantic Scholar API. |
| **openFDA (R)** | OpenFDA | CRAN: `openFDA` | R package for OpenFDA API (published July 2025). |
| **europepmc (R)** | Europe PMC | CRAN: `europepmc` | R interface to Europe PMC RESTful Web Service (rOpenSci). |
| **otargen (R)** | Open Targets | CRAN: `otargen` | R package for Open Targets Genetics API. |

### MCP Servers (Model Context Protocol)

| Server | Target API | GitHub |
|--------|-----------|--------|
| **ClinicalTrials.gov MCP** | ClinicalTrials.gov API v2 | https://github.com/cyanheads/clinicaltrialsgov-mcp-server |
| **Semantic Scholar MCP** | Semantic Scholar API | Available via PulseMCP |

### Other Tools

| Tool | Description | URL |
|------|-------------|-----|
| **EndurantDevs drug-api** | US Drugs API combining OpenFDA, RxNorm, and other sources | https://github.com/EndurantDevs/drug-api |
| **UniProt.REST (R)** | R interface to UniProt REST API | https://github.com/lgatto/UniProt.REST |
| **DisGeNET Cytoscape App** | Cytoscape plugin for disease-gene network visualization | Available via Cytoscape App Store |

---

## Summary: Priority APIs for Agentic Health

### Tier 1 -- Core (implement first)
| Resource | Use Case |
|----------|----------|
| PubMed E-utilities | Literature search and retrieval |
| medRxiv/bioRxiv API | Preprint access |
| ClinicalTrials.gov API v2 | Clinical trial search |
| OpenFDA | Drug safety and labeling data |
| RxNorm | Drug name normalization |
| UMLS / SNOMED CT / ICD | Medical terminology standardization |
| HAPI FHIR | Clinical data interoperability |

### Tier 2 -- High Value (implement next)
| Resource | Use Case |
|----------|----------|
| Semantic Scholar | AI-powered literature discovery |
| Europe PMC | European literature + text-mined annotations |
| ClinVar | Clinical variant interpretation |
| gnomAD | Population variant frequencies |
| Open Targets | Drug target identification |
| Orphanet API | Rare disease data |
| DailyMed | Drug label information |
| WHO GHO | Global health statistics |

### Tier 3 -- Supplementary
| Resource | Use Case |
|----------|----------|
| EMA Data | European drug regulatory data |
| ECDC | European disease surveillance |
| UniProt | Protein data |
| DisGeNET | Disease-gene associations |
| OMIM | Mendelian disorder catalog |
| DrugBank | Comprehensive drug data (academic access) |
| Danish Health Data Authority | Danish population health registers (restricted) |
| MeSH API | Biomedical vocabulary hierarchy |

---

## Notes on Access Patterns

1. **No authentication needed**: OpenFDA, RxNorm, bioRxiv/medRxiv, DailyMed, MeSH, UniProt, Europe PMC, WHO GHO, gnomAD, ClinicalTrials.gov
2. **Free API key required**: PubMed E-utilities (recommended), Semantic Scholar (for higher limits), ICD-11
3. **Free license/registration required**: UMLS/SNOMED CT, OMIM, DrugBank (academic)
4. **Restricted access**: Danish Health Data Authority registers (research application required)
5. **Commercial API with free data**: DrugBank (API is commercial, but data dumps are free for academics)

## Rate Limits to Note

- PubMed: 3 req/sec without key, 10 req/sec with key
- Semantic Scholar: 1000 req/sec shared (unauthenticated)
- OpenFDA: 240 req/min without key, 120,000 req/day with key
- bioRxiv/medRxiv: 100 results per page, reasonable use expected
- ClinicalTrials.gov: Reasonable use expected, no published hard limits
