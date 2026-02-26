# Health AI Agent Frameworks, Prompts, and Tools

> Research compiled 2026-02-26 for the Agentic Health project.

---

## Table of Contents

1. [Curated Awesome Lists](#1-curated-awesome-lists)
2. [MCP Servers for Health Data](#2-mcp-servers-for-health-data)
3. [Medical Prompt Libraries and Engineering](#3-medical-prompt-libraries-and-engineering)
4. [Health-Focused Agent Frameworks](#4-health-focused-agent-frameworks)
5. [Medical RAG Systems (LangChain / LlamaIndex)](#5-medical-rag-systems-langchain--llamaindex)
6. [Open-Source Health Chatbot Frameworks](#6-open-source-health-chatbot-frameworks)
7. [GPT-Based Health Projects](#7-gpt-based-health-projects)
8. [Medical AI Safety and Guardrail Frameworks](#8-medical-ai-safety-and-guardrail-frameworks)
9. [Medical LLM Collections and Foundations](#9-medical-llm-collections-and-foundations)
10. [Claude Code Skills and Tooling](#10-claude-code-skills-and-tooling)

---

## 1. Curated Awesome Lists

### Awesome-AI-Agents-for-Healthcare
- **URL:** https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare
- **Description:** Curated list of research papers, projects, and resources on agentic AI and AI agents for healthcare. Covers medical image analysis, EHR manipulation, counseling, drug discovery, patient dialogue, and healthcare administration.
- **Relevance:** High. Central reference for the entire health agent ecosystem.

### Awesome-LLM-Healthcare
- **URL:** https://github.com/mingze-yuan/Awesome-LLM-Healthcare
- **Description:** Paper list from the review "Large Language Models Illuminate a Progressive Pathway to Artificial Healthcare Assistant." Tracks LLM progress in medicine.
- **Relevance:** High. Academic resource for understanding LLM capabilities in healthcare.

### HealthcareAgent (AI-Hub-Admin)
- **URL:** https://github.com/AI-Hub-Admin/HealthcareAgent
- **Description:** List of awesome AI agents for healthcare plus a common agentic AI API interface (Python package on PyPI).
- **Relevance:** High. Provides both a curated list and a reusable API abstraction layer.

### Awesome-LLM-Agents-Scientific-Discovery
- **URL:** https://github.com/zjlrock777/Awesome-LLM-Agents-Scientific-Discovery
- **Description:** Curated list of LLM-powered AI agents in biomedical research: medical image analysis, multi-omics genomics, biomedical scientific discoveries.
- **Relevance:** Medium-high. Focused on research/discovery rather than clinical care.

### Awesome-Medical-Large-Language-Models
- **URL:** https://github.com/burglarhobbit/Awesome-Medical-Large-Language-Models
- **Description:** Curated collection of popular foundation models in healthcare with paper references.
- **Relevance:** Medium-high. Good reference for model selection.

### Awesome-Agentic-Clinical-Dialogue
- **URL:** https://github.com/xqz614/Awesome-Agentic-Clinical-Dialogue
- **Description:** Papers about methods related to agentic clinical dialogue systems.
- **Relevance:** High. Directly relevant to building conversational health agents.

### Awesome AI Agents for HCLS (AWS)
- **URL:** https://github.com/aws-samples/awesome-ai-agents-hcls
- **Description:** AWS-curated list of agentic workflows with generative AI across the health, care, and life sciences value chain.
- **Relevance:** Medium. AWS-oriented but contains broadly useful architecture references.

---

## 2. MCP Servers for Health Data

### Medical MCP Server (JamesANZ)
- **URL:** https://github.com/JamesANZ/medical-mcp
- **Description:** MCP server providing comprehensive medical information by querying FDA, WHO, PubMed, Google Scholar, and RxNorm APIs. Works with Claude Desktop and Cursor.
- **Relevance:** Very high. Drop-in MCP server for medical knowledge retrieval.

### Healthcare MCP Server (Cicatriiz)
- **URL:** https://github.com/Cicatriiz/healthcare-mcp-public
- **Description:** Node.js MCP server providing access to FDA drug info, PubMed, medRxiv, NCBI Bookshelf, clinical trials, ICD-10, DICOM metadata, and a medical calculator.
- **Relevance:** Very high. Broad coverage of healthcare data sources in a single server.

### FHIR MCP Server (Momentum)
- **URL:** https://github.com/the-momentum/fhir-mcp-server
- **Description:** Natural language interface for healthcare data built on the FHIR standard. Eliminates weeks of FHIR learning and prevents LLM hallucination of medical codes. Works with Claude, Cursor, and any MCP-compatible client.
- **Relevance:** Very high. FHIR is the dominant healthcare interoperability standard.

### Apple Health MCP Server (Momentum)
- **URL:** https://github.com/the-momentum/apple-health-mcp-server
- **Description:** MCP server for querying Apple Health data with natural language using DuckDB. Converts Apple Health XML exports into structured, queryable data.
- **Relevance:** High. Useful for personal health data analysis workflows.

### Open Wearables (Momentum)
- **URL:** https://github.com/the-momentum/open-wearables
- **Description:** Self-hosted platform to unify wearable health data from Apple Health, Samsung Health Connect, Garmin, Polar, Suunto, Whoop (Oura, Fitbit, Google Fit coming). Includes MCP server for Claude/ChatGPT integration. MIT License. 500+ GitHub stars.
- **Relevance:** Very high. Unified wearable data API with built-in MCP support.

### OMOP MCP Server (FastOMOP)
- **URL:** https://github.com/fastomop/omcp
- **Description:** MCP server for the OMOP Common Data Model. Enables LLMs to interact with OMOP-compliant healthcare databases. Converts natural language into optimized SQL queries. MIT License.
- **Relevance:** Very high. OMOP CDM is widely used for observational health research.

### OMOP Terminology MCP (OHNLP)
- **URL:** https://github.com/OHNLP/omop_mcp
- **Description:** MCP server for mapping clinical terminology to OMOP concepts using LLMs. Focused on standardized vocabulary mapping.
- **Relevance:** High. Complementary to the FastOMOP server for terminology tasks.

### 19 Free MCP Servers for Healthcare (Medevel roundup)
- **URL:** https://medevel.com/19-free-open-source-mcp-servers-for-healthcare/
- **Description:** Roundup article listing 19 open-source MCP servers for healthcare applications including DICOM, PubMed, clinical trials, and more.
- **Relevance:** High. Good meta-reference for discovering additional MCP servers.

---

## 3. Medical Prompt Libraries and Engineering

### Prompts for Health (FortaTech)
- **URL:** https://github.com/FortaTech/prompts-for-health
- **Description:** Collection of prompts to transform how healthcare professionals use generative conversational AI. Organized by use case.
- **Relevance:** Very high. Ready-to-use prompt library for health AI applications.

### AutoMedPrompt
- **URL:** https://arxiv.org/abs/2502.15944
- **Description:** Framework for optimizing LLM medical prompts using textual gradients (TextGrad). Sets SOTA on PubMedQA (82.6%), outperforms GPT-4, Claude 3 Opus, and Med-PaLM 2 on open-source models. Code is open-source.
- **Relevance:** Very high. Automated prompt optimization specifically for medical domains.

### CliniPrompt (University of Wisconsin)
- **URL:** https://cliniprompt.medicine.wisc.edu/
- **Description:** User-friendly prompt engineering and library software for health systems. Designed for clinical use.
- **Relevance:** High. Production-ready prompt library for clinical settings.

### Prompt Engineering in Clinical Practice (JMIR Tutorial)
- **URL:** https://pmc.ncbi.nlm.nih.gov/articles/PMC12439060/
- **Description:** Peer-reviewed tutorial for clinicians covering zero-shot, few-shot, chain-of-thought, self-consistency, and meta-prompting techniques in clinical settings.
- **Relevance:** High. Evidence-based guide for healthcare prompt engineering.

### Prompt Engineering as an Emerging Skill for Medical Professionals (JMIR)
- **URL:** https://pmc.ncbi.nlm.nih.gov/articles/PMC10585440/
- **Description:** Tutorial on five key principles: explicitness, contextual relevance, iterative refinement, ethical considerations, and evidence-based practices.
- **Relevance:** High. Foundational reference for medical prompt design.

### Prompt Engineering for Healthcare (ScienceDirect survey, 2025)
- **URL:** https://www.sciencedirect.com/science/article/pii/S295016282500058X
- **Description:** Comprehensive survey categorizing medical prompt engineering techniques from manual to automated, discrete to continuous.
- **Relevance:** High. Academic survey of the full landscape.

### Microsoft Promptbase
- **URL:** https://github.com/microsoft/promptbase
- **Description:** Microsoft's open-source prompt engineering toolkit. Not health-specific but includes Medprompt methodology that achieved strong medical benchmark results.
- **Relevance:** Medium-high. Medprompt is a key technique for medical LLM performance.

### Prompt Engineering in Healthcare (HealthTech Magazine)
- **URL:** https://healthtechmagazine.net/article/2025/04/prompt-engineering-in-healthcare-best-practices-strategies-trends-perfcon
- **Description:** Best practices, strategies, and trends for prompt engineering in healthcare IT.
- **Relevance:** Medium. Practitioner-oriented overview.

---

## 4. Health-Focused Agent Frameworks

### Multi-Agent Medical Assistant
- **URL:** https://github.com/souvikmajumder26/Multi-Agent-Medical-Assistant
- **Description:** GenAI-powered multi-agentic medical diagnostics and healthcare research assistance chatbot. Designed for healthcare professionals, researchers, and patients.
- **Relevance:** Very high. Purpose-built multi-agent medical system.

### AI-Agents-for-Medical-Diagnostics
- **URL:** https://github.com/ahmadvh/AI-Agents-for-Medical-Diagnostics
- **Description:** Python project creating specialized LLM-based AI agents that analyze complex medical cases. Integrates insights from various medical professionals for comprehensive assessments and personalized treatment recommendations.
- **Relevance:** Very high. Demonstrates multi-specialist agent collaboration.

### Agentic AI Workflow for Healthcare Simulation
- **URL:** https://advancesinsimulation.biomedcentral.com/articles/10.1186/s41077-025-00357-z
- **Description:** Research paper on evolving from ChatGPT prototypes to sophisticated platform implementations with multiple specialized AI agents for simulation scenario design (objective formulation, patient narrative generation, diagnostic data creation).
- **Relevance:** High. Demonstrates agentic workflow patterns for healthcare.

### CrewAI (General Framework)
- **URL:** https://www.crewai.com/open-source
- **Description:** Open-source multi-agent orchestration framework. Role-based task delegation where agents take on specialized roles. Applicable to healthcare with custom crews.
- **Relevance:** Medium-high. General framework that can be configured for health use cases.

### AutoGen (Microsoft, General Framework)
- **URL:** https://github.com/microsoft/autogen
- **Description:** Open-source framework for building agentic systems with multi-agent collaboration. Good for research and prototyping medical agent workflows.
- **Relevance:** Medium-high. Flexible enough for healthcare prototyping.

---

## 5. Medical RAG Systems (LangChain / LlamaIndex)

### Medical-RAG-LLM
- **URL:** https://github.com/AquibPy/Medical-RAG-LLM
- **Description:** Full open-source medical RAG stack using BioMistral 7B, PubMedBert for embeddings, Qdrant vector DB, LangChain and Llama CPP for orchestration.
- **Relevance:** Very high. Complete reference implementation of a medical RAG pipeline.

### MedExplainer-Langchain-RAG-LLM
- **URL:** https://github.com/manooshree/MedExplainer-Langchain-RAG-LLM
- **Description:** LangChain-based RAG system for answering medical questions using embedding distance.
- **Relevance:** High. Simpler medical RAG reference implementation.

### Llama2-Medical-Chatbot
- **URL:** https://github.com/AIAnytime/Llama2-Medical-Chatbot
- **Description:** Medical chatbot built with Llama2, Sentence Transformers, LangChain, and Chainlit. Runs on CPU with 16GB RAM minimum.
- **Relevance:** High. Demonstrates accessible local medical RAG deployment.

---

## 6. Open-Source Health Chatbot Frameworks

### Doctor-Chatbot (LifestyleCorp)
- **URL:** https://github.com/LifestyleCorp/Doctor-Chatbot
- **Description:** Multimodal, multi-agent LLM-powered open-source doctor chatbot. Can diagnose, elicit physical examination, advise investigations and management for medical ailments. MIT License.
- **Relevance:** Very high. Full-featured open-source clinical assistant.

### AI Medical Chatbot (ruslanmv)
- **URL:** https://github.com/ruslanmv/ai-medical-chatbot
- **Description:** Production-ready, enterprise-grade conversational AI for medical consultation assistance. Uses IBM WatsonX, OpenAI GPT models, and advanced RAG techniques.
- **Relevance:** High. Enterprise-grade reference architecture.

### MediMate
- **URL:** https://github.com/LakshayGMZ/MediMate
- **Description:** Personal healthcare assistant chatbot with symptom analysis and health guidance.
- **Relevance:** Medium. Lighter-weight health chatbot implementation.

### HealthCare-Chatbot (AdesharaBrijesh)
- **URL:** https://github.com/AdesharaBrijesh/HealthCare-Chatbot
- **Description:** AI-powered assistant for initial medical guidance and appointment scheduling. Uses NLP to understand symptoms, suggest conditions, and offer basic health advice.
- **Relevance:** Medium. Good template for appointment-integrated health bots.

### medicalChatBot (shaficse)
- **URL:** https://github.com/shaficse/medicalChatBot
- **Description:** Medical chatbot providing patients with personalized access to medical information using AI and NLP techniques.
- **Relevance:** Medium. Straightforward medical chatbot template.

---

## 7. GPT-Based Health Projects

### StanfordBDHG HealthGPT
- **URL:** https://github.com/StanfordBDHG/HealthGPT
- **Description:** Stanford project to query Apple Health data with natural language. Supports GPT-3.5/GPT-4 queries for sleep, step count, active energy, exercise minutes, heart rate, and body mass. iOS app built with Swift.
- **Relevance:** Very high. Stanford-backed, well-maintained personal health AI.

### MedicalGPT (shibing624)
- **URL:** https://github.com/shibing624/MedicalGPT
- **Description:** Training pipeline for medical GPT models implementing pretraining, supervised fine-tuning, RLHF, and DPO. Train your own medical language model.
- **Relevance:** High. Full training pipeline for custom medical LLMs.

### HuatuoGPT
- **URL:** https://github.com/FreedomIntelligence/HuatuoGPT
- **Description:** Open medical GPT trained on a large Chinese medical corpus. Designed for medical consultation scenarios.
- **Relevance:** Medium-high. Leading Chinese medical LLM; useful for multilingual health AI.

### HealthGPT (ZJU4HealthCare / ICML 2025 Spotlight)
- **URL:** https://github.com/DCDmllm/HealthGPT
- **Description:** Medical Large Vision-Language Model with unified framework integrating medical visual comprehension and generation capabilities. ICML 2025 Spotlight paper.
- **Relevance:** High. State-of-the-art multimodal medical AI.

### Open-Custom-GPT
- **URL:** https://github.com/SamurAIGPT/Open-Custom-GPT
- **Description:** No-code builder for GPT assistants using the Assistants API. Supports code interpreter, file retrieval, DALL-E, and custom functions. Can be adapted for health use cases.
- **Relevance:** Medium. General framework, not health-specific.

---

## 8. Medical AI Safety and Guardrail Frameworks

### NVIDIA NeMo Guardrails
- **URL:** https://github.com/NVIDIA/NeMo-Guardrails
- **Description:** Open-source toolkit for adding programmable guardrails to LLM-based systems. Supports topical guardrails, safety guardrails, fact-checking, hallucination detection, and protection against attacks. Colang modeling language for dialogue flows. Has a specific healthcare RAG example.
- **Blog:** https://developer.nvidia.com/blog/develop-secure-reliable-medical-apps-with-rag-and-nvidia-nemo-guardrails/
- **Relevance:** Very high. Leading open-source guardrails framework with explicit healthcare support.

### Enhancing Guardrails for Safe Healthcare AI (Research)
- **URL:** https://arxiv.org/html/2409.17190v1
- **Description:** Research proposing integration of NeMo Guardrails with Llama Guard for healthcare-specific safety. Addresses hallucinations, misinformation, and factual accuracy beyond what general-purpose content filters provide.
- **Relevance:** High. Architectural blueprint for healthcare-specific guardrails.

### Pharmacovigilance Guardrails (Nature Scientific Reports)
- **URL:** https://www.nature.com/articles/s41598-025-09138-0
- **Description:** Proof-of-concept guardrail suite designed to mitigate hallucinations and errors in drug safety contexts. Applicable to other medical safety-critical settings.
- **Relevance:** High. Specialized guardrails for drug safety -- a critical healthcare subdomain.

### GARAG / GAVS Frameworks
- **URL:** https://pmc.ncbi.nlm.nih.gov/articles/PMC12599997/
- **Description:** GARAG ensures management plans are grounded in peer-reviewed guideline sources. GAVS applies a similar principle to medical coding through a 2-step process: diagnostic entity generation followed by deterministic mapping to valid ontology terms.
- **Relevance:** High. Demonstrates structured guardrails for clinical guideline adherence.

---

## 9. Medical LLM Collections and Foundations

### OpenMed
- **URL:** https://huggingface.co/blog/MaziyarPanahi/openmed-year-in-review-2025
- **Description:** 380+ state-of-the-art medical models under Apache 2.0 license. Includes medical NER models covering the full spectrum of clinical text analysis, domain-adapted on 12+ public biomedical datasets. 29.7 million HuggingFace downloads.
- **Relevance:** Very high. Largest open collection of medical AI models.

### SLMs in Healthcare
- **URL:** https://github.com/drmuskangarg/SLMs-in-healthcare
- **Description:** Compressed and optimized small language models for healthcare, developed as resource-efficient alternatives to large LLMs.
- **Relevance:** Medium-high. Important for deployment in resource-constrained healthcare settings.

### Open Source HealthTech Directory (FacileTechnoLab)
- **URL:** https://www.faciletechnolab.com/blog/directory-of-open-source-healthtech-projects-and-libraries/
- **Description:** Directory of 65+ open-source health tech projects and tools for developers building medical applications.
- **Relevance:** Medium-high. Broad discovery resource.

### Best Open Source LLM for Healthcare (SiliconFlow guide)
- **URL:** https://www.siliconflow.com/articles/en/best-open-source-LLM-for-healthcare
- **Description:** Comprehensive guide comparing open-source LLMs for healthcare use in 2026 including evaluation criteria and benchmarks.
- **Relevance:** Medium-high. Useful for model selection decisions.

---

## 10. Claude Code Skills and Tooling

### Claude Code Skills System
- **URL:** https://code.claude.com/docs/en/skills
- **Description:** Claude Code supports custom skills via SKILL.md files with YAML frontmatter and markdown instructions. Skills become /slash-commands and can be auto-loaded when relevant. Health-specific skills can be created for medical coding, clinical note generation, drug interaction checks, etc.
- **Relevance:** Very high. Direct mechanism for building health-specific Claude Code extensions.

### Awesome Claude Code
- **URL:** https://github.com/hesreallyhim/awesome-claude-code
- **Description:** Curated list of skills, hooks, slash-commands, agent orchestrators, applications, and plugins for Claude Code. No health-specific skills catalogued yet, but provides the pattern for creating them.
- **Relevance:** High. Template and inspiration for building health-specific Claude Code skills.

### dotclaude.com Commands Directory
- **URL:** https://dotclaude.com/commands
- **Description:** Community directory of Claude Code slash commands. Can be used to discover and share health-related commands.
- **Relevance:** Medium. Community resource for command discovery.

---

## Summary of Top Recommendations

| Category | Top Pick | Why |
|----------|----------|-----|
| Curated List | Awesome-AI-Agents-for-Healthcare | Most comprehensive health agent list |
| MCP Server (Knowledge) | Healthcare MCP (Cicatriiz) | Broadest API coverage (FDA, PubMed, ICD-10, DICOM) |
| MCP Server (FHIR) | FHIR MCP Server (Momentum) | Standard-compliant healthcare data access |
| MCP Server (Wearables) | Open Wearables (Momentum) | Multi-device unified API with MCP |
| MCP Server (Research) | OMOP MCP (FastOMOP) | Access OMOP research databases via natural language |
| Prompt Library | Prompts for Health (FortaTech) | Ready-to-use healthcare prompt collection |
| Prompt Optimization | AutoMedPrompt | SOTA automated medical prompt optimization |
| Agent Framework | Multi-Agent Medical Assistant | Purpose-built multi-agent medical system |
| RAG System | Medical-RAG-LLM | Complete open-source medical RAG stack |
| Chatbot | Doctor-Chatbot (LifestyleCorp) | Full-featured open-source clinical assistant |
| Safety/Guardrails | NVIDIA NeMo Guardrails | Leading open-source guardrails with healthcare examples |
| Medical LLMs | OpenMed | 380+ Apache 2.0 medical models |
| Personal Health | StanfordBDHG HealthGPT | Stanford-backed Apple Health querying |
