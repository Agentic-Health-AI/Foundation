# Open-Source AI Agents for Medical/Health Research

> Research compiled: 2026-02-26
> Purpose: Directory of open-source AI agents relevant to the Agentic Health ecosystem

---

## Table of Contents

1. [Curated Lists and Awesome Repositories](#curated-lists-and-awesome-repositories)
2. [PubMed and Literature Search Agents](#pubmed-and-literature-search-agents)
3. [Preprint Search Tools (medRxiv / bioRxiv)](#preprint-search-tools-medrxiv--biorxiv)
4. [Systematic Literature Review Agents](#systematic-literature-review-agents)
5. [Clinical Trial Finder Agents](#clinical-trial-finder-agents)
6. [Drug Interaction and Drug Discovery Agents](#drug-interaction-and-drug-discovery-agents)
7. [Medical Diagnostics and Clinical Reasoning Agents](#medical-diagnostics-and-clinical-reasoning-agents)
8. [AI Health Assistants](#ai-health-assistants)
9. [Genomics and Biomarker Analysis](#genomics-and-biomarker-analysis)
10. [Multi-Source Research Assistants](#multi-source-research-assistants)
11. [Benchmarks and Evaluation](#benchmarks-and-evaluation)

---

## Curated Lists and Awesome Repositories

### Awesome-AI-Agents-for-Healthcare
- **GitHub:** https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare
- **Description:** Comprehensive curated list of research papers, projects, and resources related to agentic AI and AI agents for healthcare. Covers clinical reasoning, diagnostics, rare disease, genomics, drug discovery, and more. The single best starting point for discovering healthcare AI agents.
- **Agentic Health fit:** Central reference for the entire ecosystem. Tracks actively maintained projects, MCP servers, and frameworks.

### Awesome-AI-Agents-Medicine
- **GitHub:** https://github.com/AIM-Research-Lab/Awesome-AI-Agents-Medicine
- **Description:** Academic-oriented list of AI agents applied to medicine, covering diagnostic agents, treatment planning agents, and research agents.
- **Agentic Health fit:** Academic perspective complementing the more practitioner-focused lists.

### HealthcareAgent
- **GitHub:** https://github.com/AI-Hub-Admin/HealthcareAgent
- **Description:** Curated list of healthcare AI agents with a common agentic AI API interface specification. Aims to standardize how healthcare agents communicate.
- **Agentic Health fit:** The API interface standardization aligns with building an interoperable ecosystem of health agents.

---

## PubMed and Literature Search Agents

### PubMed MCP Server
- **GitHub:** https://github.com/cyanheads/pubmed-mcp-server
- **Description:** A Model Context Protocol (MCP) server that enables AI agents to search, retrieve, and analyze biomedical literature from PubMed via NCBI E-utilities. Includes a research agent scaffold. Supports both STDIO and HTTP transport.
- **Agentic Health fit:** Directly enables any MCP-compatible AI agent (Claude, etc.) to perform PubMed searches. Core infrastructure piece for literature-based health research agents.

### Sentinel
- **GitHub:** https://github.com/EbodShojaei/sentinel
- **Description:** AI agent that retrieves PubMed publications using phi3.5 with phidata. Generates MeSH search terms and runs them on NCBI Entrez. Supports date-range filtering.
- **Agentic Health fit:** Lightweight, self-contained PubMed search agent that demonstrates autonomous MeSH query generation.

### PubMedSummarizer
- **GitHub:** https://github.com/malbiruk/PubMedSummarizer
- **Description:** LLM assistant that searches PubMed, retrieves abstracts or full texts, and generates answers using OpenAI ChatGPT. Features a custom RAG pipeline, semantic search, and knowledge graph generation.
- **Agentic Health fit:** Goes beyond simple search by building knowledge graphs from literature, enabling deeper research workflows.

### PubMed Article Search Agent (PubMed_Agent)
- **GitHub:** https://github.com/mewz1k/PubMed_Agent (project page: https://mewz1k.github.io/PubMed_Agent/)
- **Description:** AI-powered agent using LlamaIndex and OpenAI that retrieves and summarizes recent PubMed articles based on user queries. Uses the Bio.Entrez library for PubMed access.
- **Agentic Health fit:** Simple, clean example of a PubMed search agent built on LlamaIndex.

### paperai
- **GitHub:** https://github.com/neuml/paperai
- **Description:** AI-powered tool for medical and scientific papers. Processes article repositories and generates bulk answers using LLM prompts and RAG pipelines. Can work with CORD-19 and other datasets.
- **Agentic Health fit:** Proven tool for large-scale medical literature analysis and question answering.

---

## Preprint Search Tools (medRxiv / bioRxiv)

### paperscraper
- **GitHub:** https://github.com/jannisborn/paperscraper
- **Description:** Python package for scraping publication metadata and full-text (PDF/XML) from PubMed, arXiv, medRxiv, bioRxiv, and chemRxiv. Includes citation counts from Google Scholar, impact factors, and meta-analysis plotting routines.
- **Agentic Health fit:** Essential data-gathering backend for any agent that needs to search across multiple preprint servers and PubMed simultaneously.

### medrxivr
- **GitHub:** https://github.com/ropensci/medrxivr
- **Description:** R package providing programmatic access to medRxiv and bioRxiv preprint metadata via the Cold Spring Harbour Laboratory API. Supports regex and Boolean search, BIB export, and full-text PDF download.
- **Agentic Health fit:** R-based tool for researchers who need systematic preprint searching. Good complement to Python-based agents.

### rbiorxiv
- **GitHub:** https://github.com/nicholasmfraser/rbiorxiv
- **Description:** R client for the bioRxiv API. Provides access to content data plus usage statistics (downloads per month).
- **Agentic Health fit:** Adds usage/impact metrics to preprint data, useful for prioritizing research.

---

## Systematic Literature Review Agents

### LatteReview
- **GitHub:** https://github.com/PouriaRouzrokh/LatteReview
- **Description:** Low-code Python package for automating systematic literature review processes through AI-powered agents. Model-agnostic: supports OpenAI, Gemini, Claude, Groq, and local models via Ollama. High-performance asynchronous processing.
- **Agentic Health fit:** Directly automates the most time-consuming part of health research -- systematic reviews. Multi-model support makes it flexible.

### Agent Literature Review (Arcadia Science)
- **GitHub:** https://github.com/Arcadia-Science/agent-literature-review
- **Description:** Virtual laboratory of AI agents designed to facilitate collaborative scientific research discussions and planning. Terminal-based application simulating a lab environment with multiple AI agents, each with different specialties.
- **Agentic Health fit:** Multi-agent collaborative approach to literature review mirrors how real research teams work. Novel paradigm for health research.

### LitLLM
- **GitHub:** https://github.com/LitLLM/LitLLM
- **Description:** AI-powered literature review assistant using RAG principles. Combines keyword-based and embedding-based search to query academic databases. Generates structured literature reviews.
- **Agentic Health fit:** Hybrid search approach (keyword + semantic) is well-suited for medical terminology where both exact terms and conceptual similarity matter.

### AI Literature Review Generator
- **GitHub:** https://github.com/tristan-mcinnis/AI-Literature-Review-Generator
- **Description:** Automates comprehensive literature review generation from a collection of academic PDFs using OpenAI GPT models.
- **Agentic Health fit:** Simple tool for turning a collection of papers into a coherent review.

---

## Clinical Trial Finder Agents

### TrialMatchAI
- **GitHub:** https://github.com/cbib/TrialMatchAI
- **Description:** Matches cancer patients to clinical trials based on their unique genomic and clinical profiles using AI. Uses LLMs to parse eligibility criteria and patient records. Provides chain-of-thought explanations for every recommendation.
- **Agentic Health fit:** Directly addresses the critical gap of matching patients to trials. Genomic-profile-aware matching is state of the art.

### ClinTrialFinder
- **GitHub:** https://github.com/chncwang/ClinTrialFinder
- **Description:** AI-powered clinical trial matching using GPT-4.1-mini for eligibility scoring and Perplexity AI for evidence lookup. Generates a 0-100 suitability score combining eligibility and evidence analysis. Live at clintrialfinder.info.
- **Agentic Health fit:** Production-ready clinical trial matching with scoring and evidence integration. Directly usable.

### PyTrial
- **GitHub:** https://github.com/RyanWangZf/PyTrial
- **Description:** Comprehensive Python platform for AI in drug development. Covers patient data simulation, trial site selection, trial outcome prediction, and patient-trial matching.
- **Agentic Health fit:** End-to-end platform covering the full clinical trial lifecycle with AI. Broader scope than just matching.

### AWS Patient Matching for Clinical Trials
- **GitHub:** https://github.com/aws-samples/patient-matching-of-clinical-trials-using-generative-ai
- **Description:** Demo of leveraging generative AI for cohort identification by matching patients to clinical trials using Amazon Bedrock and LLMs.
- **Agentic Health fit:** Reference architecture for cloud-deployed clinical trial matching.

---

## Drug Interaction and Drug Discovery Agents

### LLM-Drug-Interaction-Checker
- **GitHub:** https://github.com/AdarshBP/LLM-Drug-Interaction-Checker
- **Description:** Streamlit app that detects drug-drug interactions and side effects using free foundation LLMs from Hugging Face (GPT-2, GPT-J, BioGPT).
- **Agentic Health fit:** Accessible drug interaction checking using open models. Good starting point for a drug safety agent.

### DrugScan
- **GitHub:** https://github.com/Abhinay-sai-krishna/DrugScan
- **Description:** Analyzes drug interactions, determines safe dosages, and suggests alternative medications based on age and patient details. Integrates multiple datasets with NLP models. FastAPI backend with Streamlit frontend.
- **Agentic Health fit:** Comprehensive drug safety tool with patient-specific dosage analysis. Production-quality architecture.

### DeepPurpose
- **GitHub:** https://github.com/kexinhuang12345/DeepPurpose
- **Description:** Deep learning toolkit for drug-target interaction (DTI) prediction, drug property prediction, protein-protein interaction (PPI), drug-drug interaction (DDI), and protein function prediction. 15+ encoders, 50+ neural architectures, 10+ pretrained models. Published in Bioinformatics journal.
- **Agentic Health fit:** Foundational ML toolkit for drug discovery research. Can be wrapped in an agentic interface for automated drug interaction screening.

### Ersilia Model Hub
- **GitHub:** https://github.com/ersilia-os/ersilia
- **Description:** Open-source platform of pre-trained AI/ML models for infectious and neglected disease research. ~150 models for drug discovery. Nonprofit focused on equipping Global South researchers. No-code interface for running predictions.
- **Agentic Health fit:** Mission-aligned with open health. Democratizes drug discovery AI for under-resourced settings. Could be a powerful backend for agentic drug research workflows.

### DeepDrugRepurposer
- **GitHub:** https://github.com/fhooton/DeepDrugRepurposer
- **Description:** Deep learning framework for drug repurposing, identifying new therapeutic uses for existing drugs.
- **Agentic Health fit:** Drug repurposing is a high-impact area where AI agents can accelerate discovery of treatments for rare and neglected diseases.

### HySonLab Drug Interactions
- **GitHub:** https://github.com/HySonLab/drug-interactions
- **Description:** Research project on drug interactions published at NeurIPS 2022 (AI for Science track). Graph-based approaches to predicting drug-drug interactions.
- **Agentic Health fit:** State-of-the-art research models that could power drug interaction checking agents.

---

## Medical Diagnostics and Clinical Reasoning Agents

### OpenMedicine
- **GitHub:** https://github.com/RamosFBC/openmedicine
- **Description:** Open-source Python library and MCP Server providing deterministic, DOI-traceable clinical reasoning for AI agents. Every calculator, score, and guideline returns its scientific source. Outputs include LOINC/SNOMED codes for EHR integration. Pydantic models validate all clinical inputs.
- **Agentic Health fit:** Critical infrastructure for evidence-based health agents. Forces agents to cite verified clinical standards rather than relying on hallucinated medical knowledge. MCP server architecture makes it pluggable.

### Medical Deep Research
- **GitHub:** https://github.com/Clinical-Copilot/Medical_Deep_Research
- **Description:** Open-source agentic system for comprehensive medical and clinical investigations. Converges LLMs, advanced reasoning, and information retrieval for expert-level medical inquiry. Supports MCP with automatic resource discovery. Access to full-text articles and specialized medical repositories.
- **Agentic Health fit:** The "deep research" paradigm applied specifically to medicine. MCP support makes it composable with other health agents.

### Multi-Agent Medical Assistant
- **GitHub:** https://github.com/souvikmajumder26/Multi-Agent-Medical-Assistant
- **Description:** GenAI-powered multi-agentic medical diagnostics and healthcare research assistance chatbot. Designed for healthcare professionals, researchers, and patients. Multiple specialized agents collaborate on diagnoses.
- **Agentic Health fit:** Multi-agent architecture where different specialists collaborate mirrors real clinical team dynamics.

### AI-Agents-for-Medical-Diagnostics
- **GitHub:** https://github.com/ahmadvh/AI-Agents-for-Medical-Diagnostics
- **Description:** Python project creating specialized LLM-based AI agents that analyze complex medical cases. Integrates insights from various simulated medical professionals for comprehensive assessments and personalized treatment recommendations.
- **Agentic Health fit:** Demonstrates multi-specialist AI consultation pattern applicable to complex diagnostic scenarios.

### Awesome-Agentic-Clinical-Dialogue
- **GitHub:** https://github.com/xqz614/Awesome-Agentic-Clinical-Dialogue
- **Description:** Resource collection of medical agents for clinical dialogue and health conversations.
- **Agentic Health fit:** Covers the conversational/dialogue aspect of medical AI agents.

---

## AI Health Assistants

### OpenHealth
- **GitHub:** https://github.com/OpenHealthForAll/open-health
- **Stars:** ~3,800
- **Description:** AI health assistant powered by personal health data. Integrates clinical records, blood tests, health checkups, family history, and symptoms. Supports local execution via Ollama for maximum privacy. Compatible with LLaMA, DeepSeek, GPT, Claude, and Gemini.
- **Agentic Health fit:** Privacy-first, multi-model health assistant. High star count indicates strong community interest. Local execution capability is important for health data privacy.

### Aiden (AI Health Assistant)
- **GitHub:** https://github.com/louis030195/ai-health-assistant
- **Description:** Personal AI-powered health assistant providing daily insights and prompts based on health data, goals, and lifestyle to help build healthy habits.
- **Agentic Health fit:** Consumer-facing health agent focused on daily wellness and habit building.

### AI-HealthCare-Assistant
- **GitHub:** https://github.com/ahlem-phantom/AI-HealthCare-Assistant
- **Description:** Full-stack AI-powered healthcare web application combining ML, blockchain medical records, facial recognition, symptom detection, nearest doctor search, and X-ray diagnosis. Built with React, Node.js, Python, Flask, MongoDB, and Ethereum.
- **Agentic Health fit:** Ambitious full-stack health platform. Blockchain medical records aspect is interesting for data sovereignty.

---

## Genomics and Biomarker Analysis

### Claude Scientific Skills (Genomics)
- **GitHub:** https://github.com/K-Dense-AI/claude-scientific-skills
- **Description:** Ready-to-use agent skills for research and science. Includes variant database management, gene discovery via NCBI Gene/UniProt/Ensembl, network analysis for protein-protein interactions, and biomarker discovery capabilities.
- **Agentic Health fit:** Plug-and-play genomics skills for Claude-based agents. Directly relevant for biomarker and genomics research workflows.

### Scientific Skills (yorkeccak)
- **GitHub:** https://github.com/yorkeccak/scientific-skills
- **Description:** Natural language scientific literature search skills with semantic search over PubMed, arXiv, ChEMBL, DrugBank, bioRxiv, medRxiv, clinical trials, and more. Zero API complexity.
- **Agentic Health fit:** Unified search across all major health/science databases through natural language. Excellent building block for research agents.

### Nucleotide Transformer
- **GitHub:** https://github.com/instadeepai/nucleotide-transformer
- **Description:** Foundation models for genomics and transcriptomics by InstaDeep. Includes a conversational agent for interactive exploration of genomic data through natural language.
- **Agentic Health fit:** Foundation model for DNA/RNA analysis with a conversational interface. Enables natural-language genomics research.

### OmicVerse
- **GitHub:** https://github.com/Starlitnightly/omicverse
- **Description:** Python library for multi-omics analysis including bulk, single-cell, and spatial RNA-seq analysis.
- **Agentic Health fit:** Comprehensive omics analysis toolkit that could serve as a backend for genomics research agents.

### Open Omics Acceleration Framework (Intel)
- **GitHub:** https://github.com/IntelLabs/Open-Omics-Acceleration-Framework
- **Description:** Intel Labs' open-source framework for accelerating digital biology. Containerized and customizable for genomics workflows.
- **Agentic Health fit:** Performance-optimized omics computation. Useful as infrastructure for agents processing large genomic datasets.

---

## Multi-Source Research Assistants

### Copilot4Researcher
- **GitHub:** https://github.com/Witivio/Copilot4Researcher
- **Description:** Azure-powered research assistant that aggregates data from PubMed, bioRxiv, and clinical trials into a unified interface for life sciences research.
- **Agentic Health fit:** Multi-source research aggregation is exactly what health research agents need. Combines literature with clinical trial data.

### MedLLMs Practical Guide
- **GitHub:** https://github.com/AI-in-Health/MedLLMsPracticalGuide
- **Description:** Published in Nature Reviews Bioengineering. Comprehensive guide to applying LLMs in medicine. Includes Medical LLMs Tree, comparison tables, and curated papers.
- **Agentic Health fit:** Essential reference for understanding which medical LLMs to use as the foundation for health agents.

---

## Benchmarks and Evaluation

### AgentClinic
- **Website:** https://agentclinic.github.io/
- **Description:** First open-source benchmark to evaluate LLMs operating as agents in simulated clinical environments. Multimodal agent benchmark for clinical AI.
- **Agentic Health fit:** Critical for evaluating and comparing health agents. Standardized benchmarking enables quality assurance of medical AI agents.

---

## Summary and Recommendations for Agentic Health

### High-Priority Projects (most directly relevant)

| Project | Category | Why Priority |
|---------|----------|-------------|
| PubMed MCP Server | Literature Search | MCP-native, pluggable into any agent |
| OpenMedicine | Clinical Reasoning | Evidence-based, DOI-traceable, MCP server |
| Medical Deep Research | Deep Research | Agentic medical investigation with MCP |
| TrialMatchAI | Clinical Trials | Genomic-aware patient-trial matching |
| LatteReview | Literature Review | Automated systematic reviews, multi-model |
| OpenHealth | Health Assistant | Privacy-first, 3.8k stars, active community |
| paperscraper | Data Gathering | Multi-source preprint/PubMed scraping |
| Ersilia Model Hub | Drug Discovery | 150+ models, Global South focus |
| DeepPurpose | Drug Interactions | Published toolkit, 50+ architectures |
| Scientific Skills | Multi-Database Search | Unified search across all health databases |

### Architecture Patterns Observed

1. **MCP Server Pattern:** OpenMedicine, PubMed MCP Server, and Medical Deep Research all use the Model Context Protocol, enabling composable agent architectures.
2. **Multi-Agent Pattern:** Multi-Agent Medical Assistant and AI-Agents-for-Medical-Diagnostics use multiple specialized agents collaborating on medical tasks.
3. **RAG Pipeline Pattern:** PubMedSummarizer, LitLLM, and paperai use retrieval-augmented generation for evidence-based answers.
4. **Scoring/Ranking Pattern:** ClinTrialFinder and TrialMatchAI produce numerical scores for clinical trial eligibility.

### Gaps Identified

- **Rare disease agents:** Few dedicated open-source agents exist; RareAgents is mentioned in literature but no prominent GitHub project found.
- **Real-time adverse event monitoring:** No open-source agent found for real-time pharmacovigilance.
- **Patient-facing agents with clinical guardrails:** Most projects are researcher-facing; few combine accessibility with safety.
- **Wearable/IoT health data agents:** Limited open-source agents that ingest real-time health device data.
