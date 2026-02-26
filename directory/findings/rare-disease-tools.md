# Rare Disease Open-Source Tools Directory

> Research compiled: 2026-02-26
> Purpose: Catalog open-source projects relevant to rare disease diagnosis, treatment, and advocacy for the Agentic Health ecosystem.

---

## Table of Contents

1. [Rare Disease Diagnosis AI Tools](#1-rare-disease-diagnosis-ai-tools)
2. [Phenotype-to-Gene Matching Tools](#2-phenotype-to-gene-matching-tools)
3. [Rare Disease Knowledge Bases and APIs](#3-rare-disease-knowledge-bases-and-apis)
4. [Genetic Variant Interpretation Tools](#4-genetic-variant-interpretation-tools)
5. [Patient Registry and Community Platforms](#5-patient-registry-and-community-platforms)
6. [Patient Advocacy Tech Tools](#6-patient-advocacy-tech-tools)
7. [Drug Repurposing Tools](#7-drug-repurposing-tools)
8. [Undiagnosed Disease Program Tools](#8-undiagnosed-disease-program-tools)
9. [LHON and Mitochondrial Disease Tools](#9-lhon-and-mitochondrial-disease-tools)
10. [Data Standards and Interoperability](#10-data-standards-and-interoperability)

---

## 1. Rare Disease Diagnosis AI Tools

### DeepRare
- **URL**: https://www.nature.com/articles/s41586-025-10097-9 (paper); web application available but no public GitHub repo found
- **Description**: Multi-agent system for rare disease differential diagnosis powered by LLMs, integrating 40+ specialized tools and knowledge sources. Processes free-text clinical descriptions, structured HPO terms, and VCF genetic data to generate ranked diagnostic hypotheses with transparent, evidence-linked reasoning.
- **Performance**: 64.4% first-attempt accuracy vs 54.6% for experienced physicians across 2,919 rare diseases. 95.4% evidence factuality agreement with clinical experts.
- **Relevance**: State-of-the-art agentic AI system for rare disease diagnosis. Directly relevant to Agentic Health's mission. Architecture of multi-agent + tool integration is a model for agentic health systems. No open-source code found yet.

### SHEPHERD
- **URL**: https://github.com/mims-harvard/SHEPHERD
- **Description**: Few-shot learning approach for phenotype-driven diagnosis of patients with rare genetic diseases. Uses knowledge-grounded metric learning on a rare disease knowledge graph. Supports causal gene discovery, patients-like-me identification, and novel disease characterization.
- **Performance**: Trained on simulated patients, evaluated on 465 patients from the Undiagnosed Diseases Network. Causal genes predicted at rank 3.52 on average.
- **License**: Open source (PyTorch implementation)
- **Relevance**: High. Directly applicable to rare disease diagnosis. Knowledge graph approach is compatible with agentic systems. Published in npj Digital Medicine (2025).

---

## 2. Phenotype-to-Gene Matching Tools

### Exomiser
- **URL**: https://github.com/exomiser/Exomiser
- **Description**: The most widely adopted open-source tool for prioritizing coding and noncoding variants in rare disease. Performs integrative analysis of patient sequencing data and HPO-encoded phenotypes. Leverages variant frequency, predicted pathogenicity, gene-phenotype associations from human diseases, model organisms, and protein-protein interactions.
- **License**: Open source (Java)
- **Relevance**: Gold standard tool for phenotype-driven variant prioritization. Used in the 100,000 Genomes Project. Essential reference for any rare disease genomics pipeline.

### LIRICAL
- **URL**: https://github.com/TheJacksonLaboratory/LIRICAL
- **Description**: LIkelihood Ratio Interpretation of Clinical AbnormaLities. Provides clinically interpretable analysis of HPO-encoded phenotypic abnormalities, optionally combined with VCF variant data. Outputs human-friendly HTML reports breaking down HPO term and variant contributions per diagnosis.
- **License**: Open source (Java, from Jackson Laboratory)
- **Relevance**: High. Complements Exomiser with a likelihood-ratio approach. Produces interpretable clinical reports, useful for agentic systems that need to explain reasoning.

### Phenomiser
- **URL**: https://github.com/TheJacksonLaboratory/Phenomiser
- **Description**: Phenotype-based diagnosis tool for rare diseases from Jackson Laboratory. Works with Phenopackets standard.
- **License**: Open source
- **Relevance**: Part of the Jackson Lab rare disease tooling ecosystem alongside LIRICAL and Exomiser.

### PatientMatcher
- **URL**: https://github.com/Clinical-Genomics/patientMatcher
- **Description**: Open-source Python/MongoDB tool for matching undiagnosed rare disease patients via the Matchmaker Exchange network. Computes similarity scores based on genotype (GTScore) and phenotype (PhenoScore).
- **License**: Open source (Python)
- **Relevance**: Enables cross-institutional patient matching for unsolved rare disease cases. Key infrastructure for collaborative diagnosis.

### Matchbox
- **URL**: https://github.com/macarthur-lab/matchbox
- **Description**: Platform-independent bridge between rare disease genomic centers and the Matchmaker Exchange network. Has led to novel gene discoveries.
- **License**: Open source
- **Relevance**: Enables any genomic center to participate in the global Matchmaker Exchange network for rare disease gene discovery.

### Matchmaker Exchange API
- **URL**: https://github.com/ga4gh/mme-apis
- **Description**: Protocol and data format specification for exchanging phenotype and genotype profiles across patient databases to facilitate rare disease matchmaking.
- **License**: Open source (GA4GH standard)
- **Relevance**: Foundational API standard for federated rare disease patient matching.

---

## 3. Rare Disease Knowledge Bases and APIs

### Monarch Initiative
- **URL**: https://github.com/monarch-initiative | https://monarchinitiative.org/
- **Description**: International consortium providing a knowledge graph of millions of entities (genes, diseases, phenotypes) from dozens of sources. Includes monarch-app (Vue webapp + Python API), monarchr (R package), and the Monarch Knowledge Graph.
- **License**: Open source
- **Relevance**: Very high. Central knowledge graph for rare disease research. Provides APIs (monarch-py, FastAPI backend) that could be integrated into agentic health systems. Actively maintained with major 2025 updates.

### Orphadata / Orphanet
- **URL**: https://www.orphadata.com/ | https://github.com/orphanet-rare-diseases-issues/API_V1
- **Description**: Comprehensive rare disease knowledge base. Orphadata provides bulk datasets under CC BY 4.0 license. Cross-referenced with OMIM, ICD-10, MeSH, MedDRA, UMLS, GARD, HGNC, UniProtKB. API available at api.orphacode.org.
- **License**: CC BY 4.0 (data); API available
- **Relevance**: Very high. Authoritative rare disease nomenclature and classification. Essential data source for any rare disease AI system.

### ORDO (Orphanet Rare Disease Ontology)
- **URL**: https://www.orphadata.com/ordo/ | https://bioportal.bioontology.org/ontologies/ORDO
- **Description**: Structured vocabulary for rare diseases capturing relationships between diseases, genes, and other features. Derived from the Orphanet knowledge base.
- **License**: Open (via BioPortal)
- **Relevance**: Standard ontology for rare diseases. Essential for data harmonization and interoperability.

### Human Phenotype Ontology (HPO)
- **URL**: https://github.com/obophenotype/human-phenotype-ontology | https://hpo.jax.org/
- **Description**: Standardized vocabulary of 18,000+ hierarchically organized terms for phenotypic abnormalities in human disease. Used in thousands of exome/genome sequencing projects worldwide.
- **License**: Open source
- **Relevance**: Foundational ontology for rare disease phenotyping. Required by Exomiser, LIRICAL, DeepRare, and virtually all rare disease AI tools.

### HPOExplorer
- **URL**: https://github.com/neurogenomics/HPOExplorer
- **Description**: R package for importing, annotating, filtering, and visualizing HPO data. Available via DockerHub.
- **License**: Open source (R)
- **Relevance**: Useful for exploring and working with HPO data programmatically.

### OMIM API
- **URL**: https://www.omim.org/help/api
- **Description**: API for Online Mendelian Inheritance in Man, providing access to information on all known Mendelian disorders and 15,000+ genes. Updated daily.
- **License**: API access available (registration required)
- **Relevance**: Critical reference database for genetic disorders. API enables programmatic access for agentic systems.

### GARD Knowledge Graph
- **URL**: https://pmc.ncbi.nlm.nih.gov/articles/PMC7663894/ (described in paper)
- **Description**: Integrative knowledge graph derived from the Genetic and Rare Diseases Information Center (GARD) at NIH.
- **License**: Public/research use
- **Relevance**: NIH-backed rare disease knowledge graph. Complements Monarch and Orphanet.

---

## 4. Genetic Variant Interpretation Tools

### AnFiSA
- **URL**: https://github.com/ForomePlatform/anfisa
- **Description**: Open-source variant curation tool bridging genetic research and clinical settings. Features multidimensional DBMS for genomic data, curated decision trees for clinical guidelines, and crowdsourcing-friendly interface for difficult cases.
- **License**: Apache 2.0
- **Relevance**: High. Purpose-built for rare disease variant analysis. Decision tree approach aligns well with agentic systems that need explainable clinical reasoning.

### AnnotateVariants
- **URL**: https://github.com/Phillip-a-richmond/AnnotateVariants
- **Description**: Pipeline for variant annotation in diagnosis of rare genetic disorders. Relies on open-source data with installation instructions.
- **License**: Open source
- **Relevance**: Practical pipeline for rare disease variant annotation.

### RareInsight
- **URL**: https://github.com/omicscodeathon/rareinsight
- **Description**: Open-source interactive dashboard to enhance accessibility, comprehension, and collaboration around genetic data for patients, caregivers, clinicians, and researchers.
- **License**: Open source
- **Relevance**: Patient-facing genetic data communication tool. Aligns with Agentic Health's goal of empowering patients.

### precisionFDA
- **URL**: https://github.com/FDA/precisionFDA
- **Description**: FDA's cloud-based platform for testing, piloting, and benchmarking NGS analysis pipelines. Ruby on Rails webapp with CLI uploader. Open to researchers, clinicians, regulators, and patient advocacy groups.
- **License**: Open source
- **Relevance**: Regulatory-grade platform for validating genomic analysis. Relevant for quality assurance in rare disease genomics pipelines.

---

## 5. Patient Registry and Community Platforms

### Rare Disease Registry Framework (RDRF)
- **URL**: https://github.com/muccg/rdrf | https://muccg.github.io/rdrf/
- **Description**: Open-source tool for rapid creation of web-based patient registries. Supports contact registries and complex registries with user group restrictions. Captures symptoms, treatments, medicines, coping mechanisms, and devices.
- **License**: Open source
- **Relevance**: High. Directly enables creation of disease-specific patient registries. Could be integrated with agentic health tools.

### OSSE (Open Source Registry System for Rare Diseases)
- **URL**: https://www.researchgate.net/publication/272663697_OSSE_-_open_source_registry_software_solution
- **Description**: Modular registry software toolkit enabling creation of rare disease registries with basic IT skills. Supports interoperability between registries at national and international levels. Used since 2016 for registries including NEOCYST.
- **License**: Open source
- **Relevance**: EU-focused open-source registry system. Designed for federation of registries across borders.

### RARE-X
- **URL**: https://rare-x.org/
- **Description**: Patient-driven data collection and sharing platform. Building the largest collaborative rare disease federated data sharing library. Data is de-identified, structured at individual patient level. Partnered with Broad Institute.
- **License**: Platform (not open source code, but open data access model)
- **Relevance**: Important data sharing infrastructure. Open Science Data Challenge model could inform Agentic Health approaches.

### OpenMOVR
- **URL**: https://openmovr.github.io/
- **Description**: Open-source tools for neuromuscular disease research, including MOVR DataHub Analytics Python library for research data access.
- **License**: Open source
- **Relevance**: Disease-specific open-source research platform. Model for other rare disease communities.

### Synthetic Rare Disease Datasets
- **URL**: https://github.com/iaBIH/synth-md
- **Description**: Code and data for generating synthetic datasets for open software development in rare disease research.
- **License**: Open source
- **Relevance**: Enables development and testing of rare disease tools without patient data privacy concerns.

---

## 6. Patient Advocacy Tech Tools

### RareCamp / OpenTreatments
- **URL**: https://rarecamp.org/ | https://www.opentreatments.org/
- **Description**: Linux Foundation project providing open-source project management tools for patient-led gene therapy development. Built with NextJS frontend and AWS serverless backend. Enables patient organizations to develop AAV gene therapy treatments for any monogenic rare disease.
- **License**: Apache 2.0
- **Relevance**: Very high. Unique open-source platform empowering patients to drive their own treatment development. Directly aligns with Agentic Health's patient empowerment mission.

### PatientsRegistryAPI (Hack the Rare)
- **URL**: https://github.com/favourori/PatientsRegistryAPI
- **Description**: Built during "Hack the Rare" hackathon organized with OpenTreatments Foundation. API for patient registries.
- **License**: Open source
- **Relevance**: Hackathon output demonstrating community-driven rare disease tool development.

---

## 7. Drug Repurposing Tools

### drexml (DRExM3L)
- **URL**: https://github.com/loucerac/drexml
- **Description**: Python CLI tool and package for drug repurposing using explainable machine learning and mechanistic models of signal transduction. Identifies drug targets capable of regulating disease pathways. Validated on Fanconi Anemia and Familial Melanoma.
- **License**: MIT
- **Relevance**: High. Directly targets rare disease drug repurposing with explainable AI. Python package makes it easy to integrate.

### NCATS Drug Repurposing Pipeline
- **URL**: https://github.com/ncats/drug_rep
- **Description**: NIH NCATS analytical pipeline using open-source chemical databases to identify novel compound-gene target relationships for rare disease drug prioritization. Uses RDKit for cheminformatics.
- **License**: Open source (NIH/NCATS)
- **Relevance**: NIH-backed drug repurposing pipeline specifically for rare diseases.

### Automated Drug Repurposing Pipeline for Rare Diseases
- **URL**: https://github.com/NCMBianchi/DrugRepurposing
- **Description**: Modular automated pipeline using Knowledge Graphs and ML. Built with Jupyter Notebook, Docker-compose, Flask, Monarch API, DGIdb API, RDKit, Node2vec, XGBoost, and PyTorch Geometric.
- **License**: Open source
- **Relevance**: High. Integrates multiple APIs (including Monarch) for automated rare disease drug repurposing. Docker-based deployment.

### DRKG (Drug Repurposing Knowledge Graph)
- **URL**: https://github.com/gnn4dr/DRKG
- **Description**: Knowledge graph and GNN-based tools for drug repurposing. Originally demonstrated on COVID-19 but applicable to rare diseases.
- **License**: Open source
- **Relevance**: General drug repurposing infrastructure applicable to rare diseases.

---

## 8. Undiagnosed Disease Program Tools

### Matchmaker Exchange
- **URL**: https://www.matchmakerexchange.org/
- **Description**: Federated network bridging patient databases to match genotypic and phenotypic characteristics across clinical facilities for unsolved rare disease cases. Multiple open-source nodes (PatientMatcher, Matchbox) listed above.
- **Relevance**: Critical infrastructure for the Undiagnosed Diseases Network. Open API standard enables agentic system integration.

### UDN Data Infrastructure
- **Description**: The Undiagnosed Diseases Network (UDN) includes sequencing cores, metabolomics core, model organisms core, and a central biorepository. The UDN Data Management and Coordinating Center (DMCC) provides infrastructure for clinical sites and research cores.
- **URL**: https://commonfund.nih.gov/Diseases
- **Relevance**: Context for understanding the computational infrastructure around undiagnosed diseases. Tools are primarily institutional rather than open source.

---

## 9. LHON and Mitochondrial Disease Tools

### MToolBox
- **URL**: https://github.com/mitoNGS/MToolBox
- **Description**: Bioinformatics pipeline for analyzing mtDNA from NGS data. Provides pathogenicity scores, genome variability profiles, and disease associations for mitochondrial variants. Outputs VCF with allele-specific heteroplasmy.
- **License**: Open source
- **Relevance**: High for LHON (a mitochondrial disease). Can analyze the three primary LHON mtDNA mutations (m.3460G>A, m.11778G>A, m.14484T>C). Directly relevant to LHONOpenClaw project.

### maegatk
- **URL**: https://github.com/caleblareau/maegatk
- **Description**: Mitochondrial Alteration Enrichment and Genome Analysis Toolkit. Python CLI for processing BAM files with mitochondrial reads and generating heteroplasmy estimates from sequencing data.
- **License**: Open source (Python)
- **Relevance**: Useful for LHON heteroplasmy analysis, which affects disease penetrance and severity.

### Himito
- **URL**: https://www.biorxiv.org/content/10.1101/2025.11.03.686348v1.full (preprint)
- **Description**: Graph-based toolkit for analyzing mitochondrial genomes using long reads. Filters NUMTs, constructs sequence graphs, assembles haplotypes, calls variants, and analyzes 5mC modifications.
- **License**: Open source (preprint stage)
- **Relevance**: Next-generation mitochondrial genome analysis. Long-read sequencing approach could improve LHON variant detection.

### MITOMAP
- **URL**: https://www.mitomap.org/
- **Description**: Database of human mitochondrial DNA variants and their association with disease, including LHON-specific variant annotations.
- **License**: Public resource
- **Relevance**: Reference database for LHON variant interpretation.

---

## 10. Data Standards and Interoperability

### GA4GH Phenopackets
- **URL**: https://obophenotype.github.io/human-phenotype-ontology/phenopackets/
- **Description**: Standard for sharing disease and phenotype information characterizing individual persons or biosamples. Flexible schema for rare disease, complex disease, and cancer.
- **License**: Open standard (GA4GH)
- **Relevance**: Critical interoperability standard. Used by Exomiser, LIRICAL, and many rare disease tools.

### PhenopacketGenerator
- **URL**: https://github.com/TheJacksonLaboratory/PhenopacketGenerator
- **Description**: Tool to generate Phenopackets for use with LIRICAL or Exomiser.
- **License**: Open source
- **Relevance**: Bridges clinical data to standardized phenopacket format for computational analysis.

### Rare Disease Common Data Model (RD-CDM)
- **URL**: https://github.com/BIH-CEI/rd-cdm
- **Description**: Ontology-based common data model harmonizing international registries, HL7 FHIR v4.0.1, and GA4GH Phenopacket v2.0 for structured data exchange.
- **License**: Open source
- **Relevance**: High. Enables interoperability across rare disease registries and clinical systems. FHIR compatibility is important for health system integration.

### Phenotools
- **URL**: https://github.com/pnrobinson/phenotools
- **Description**: C++ library for validation and processing of Phenopackets. Decodes JSON format, performs QC, and outputs summaries.
- **License**: Open source (C++)
- **Relevance**: Utility for Phenopacket validation in production pipelines.

---

## Summary and Recommendations for Agentic Health

### Highest Priority Integrations
1. **Monarch Initiative** - Central knowledge graph with Python API, ideal backbone for agentic health systems
2. **Exomiser + LIRICAL** - Gold standard phenotype-to-gene tools, essential for diagnosis agents
3. **HPO** - Required ontology for phenotype encoding across all tools
4. **Orphadata API** - Authoritative rare disease nomenclature and classification
5. **RareCamp/OpenTreatments** - Patient empowerment platform aligned with Agentic Health mission

### Key Architecture Patterns
- **DeepRare** demonstrates that multi-agent + 40-tool integration achieves state-of-the-art rare disease diagnosis
- **Matchmaker Exchange** shows how federated APIs enable cross-institutional collaboration
- **GA4GH Phenopackets** provide the interoperability standard for connecting tools
- **RD-CDM** bridges registries, FHIR, and Phenopackets for health system integration

### LHON-Specific Recommendations (for LHONOpenClaw)
- **MToolBox** for mtDNA variant analysis including LHON mutations
- **maegatk** for heteroplasmy estimation relevant to LHON penetrance
- **MITOMAP** as reference database for LHON variant annotation
- **Exomiser** can be configured for mitochondrial variant prioritization

### Gaps and Opportunities
- No dedicated open-source LHON management tools exist -- LHONOpenClaw fills a real gap
- DeepRare is not yet open source -- opportunity for open alternative
- Patient-facing AI tools for rare disease are scarce -- RareInsight is early-stage
- Drug repurposing pipelines exist but lack integration with diagnosis tools
- No unified agentic platform connects diagnosis, registry, advocacy, and treatment tools -- this is the Agentic Health opportunity
