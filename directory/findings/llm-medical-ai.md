# Open-Source LLM-Based Medical AI Projects

> Research compiled for the Agentic Health project. Last updated: 2026-02-26.

---

## Table of Contents

1. [Medical Large Language Models](#medical-large-language-models)
2. [Multimodal Medical Models](#multimodal-medical-models)
3. [Medical Chatbots and QA Systems](#medical-chatbots-and-qa-systems)
4. [Medical RAG Systems](#medical-rag-systems)
5. [Agentic Medical AI Frameworks](#agentic-medical-ai-frameworks)
6. [Clinical Decision Support Tools](#clinical-decision-support-tools)
7. [Biomedical NLP Foundation Models](#biomedical-nlp-foundation-models)
8. [MCP Servers and Claude/GPT-Based Health Tools](#mcp-servers-and-claudegpt-based-health-tools)
9. [Benchmarks and Evaluation](#benchmarks-and-evaluation)
10. [Curated Lists and Meta-Resources](#curated-lists-and-meta-resources)

---

## Medical Large Language Models

### Meditron
- **GitHub:** https://github.com/epfLLM/meditron
- **Description:** Suite of open-source medical LLMs (Meditron-7B and Meditron-70B) adapted from Llama-2 through continued pretraining on a curated medical corpus including PubMed papers, abstracts, and medical guidelines. Designed to democratize access to medical LLMs and enhance clinical decision-making.
- **Base Model:** Llama-2 (7B and 70B)
- **Relevance:** High. One of the most prominent open-source medical LLMs; direct Med-PaLM alternative.

### OpenBioLLM
- **Hugging Face:** https://huggingface.co/blog/aaditya/openbiollm
- **Description:** Advanced open-source biomedical LLM developed by Saama AI Labs. Available in 70B and 8B parameter versions, trained on a curated dataset spanning 3,000+ healthcare topics and 10+ medical subjects. Claims to outperform GPT-4, Gemini, Med-PaLM-1, and Med-PaLM-2 on biomedical benchmarks.
- **Base Model:** Llama-3 (8B and 70B)
- **Relevance:** Very high. Top-performing open-source Med-PaLM alternative.

### PMC-LLaMA
- **GitHub:** https://github.com/chaoyi-wu/PMC-LLaMA
- **Description:** Open-source language model for medicine. Pretrained with domain corpus and then tuned with instruction-following datasets. PMC_LLaMA_13B is the latest model, finetuned on medical instructions.
- **Base Model:** LLaMA (7B, 13B)
- **Relevance:** High. Foundational medical LLM with strong PubMed domain knowledge.

### BioMistral
- **GitHub:** https://github.com/BioMistral/BioMistral
- **Hugging Face:** https://huggingface.co/BioMistral/BioMistral-7B
- **Description:** Open-source LLM tailored for the biomedical domain. Further pre-trained on PubMed Central. Best performing open-source medical LLM in its weight class, with multilingual benchmark support.
- **Base Model:** Mistral-7B
- **Relevance:** High. Lightweight, performant medical LLM suitable for RAG and agent pipelines.

### MedAlpaca
- **GitHub:** https://github.com/kbressem/medAlpaca
- **Description:** Suite of LLMs fine-tuned for medical question-answering and dialogue. Trained on medical flashcards, wikis, and dialogue datasets. Expands on Stanford Alpaca and AlpacaLoRA for medical applications.
- **Base Model:** LLaMA (7B, 13B)
- **Relevance:** High. Well-established medical QA model with multiple size variants.

### Hippocrates (Hippo)
- **Website:** https://cyberiada.github.io/Hippocrates/
- **Description:** Open-source LLM framework for the medical domain offering unrestricted access to training data, codebase, checkpoints, and evaluation protocols. Introduces Hippo, a family of 7B models that outperform existing open medical LLMs by a large margin, even surpassing 70B-parameter models.
- **Base Model:** Mistral-7B and LLaMA-2-7B
- **Relevance:** High. Fully open and transparent medical LLM ecosystem.

### HuatuoGPT (Series)
- **GitHub (v1):** https://github.com/FreedomIntelligence/HuatuoGPT
- **GitHub (v2):** https://github.com/FreedomIntelligence/HuatuoGPT-II
- **GitHub (o1):** https://github.com/FreedomIntelligence/HuatuoGPT-o1
- **Description:** Family of medical LLMs. HuatuoGPT-7B and 13B are trained on Chinese medical corpus. HuatuoGPT-II achieves state-of-the-art in Chinese medical applications. HuatuoGPT-o1 focuses on complex medical reasoning (chain-of-thought style).
- **Base Model:** Baichuan-7B, Ziya-LLaMA-13B (v1); various (v2, o1)
- **Relevance:** High. Leading Chinese-language medical LLM family with reasoning capabilities.

### ChatDoctor
- **GitHub:** https://github.com/Kent0n-Li/ChatDoctor
- **Description:** Medical chat model fine-tuned on LLaMA using medical domain knowledge. Trained on HealthCareMagic-100K dataset, tested on iCliniq-10k. Aims to provide intelligent healthcare companionship for medical queries.
- **Base Model:** LLaMA
- **Relevance:** Medium-high. Early and influential medical chatbot model.

### DoctorGPT
- **GitHub:** https://github.com/tmc/DoctorGPT
- **Description:** LLM that can pass the US Medical Licensing Exam. Works offline, cross-platform, and keeps health data private. Only 3GB in size, fits on local devices. Available on iOS, Android, and Web.
- **Base Model:** Llama-2-7B (fine-tuned with RLHF and Constitutional AI)
- **Relevance:** High. Privacy-focused, runs locally, cross-platform medical LLM.

### MMedLM (Multilingual Medical LLM)
- **GitHub:** https://github.com/MAGIC-AI4Med/MMedLM
- **Description:** Published in Nature Communications. Multilingual language model for medicine, supporting multiple languages for medical applications.
- **Base Model:** Various
- **Relevance:** Medium-high. Important for non-English medical AI applications.

### OpenMed
- **Hugging Face Blog:** https://huggingface.co/blog/MaziyarPanahi/openmed-year-in-review-2025
- **Description:** Launched July 2025 with 380+ state-of-the-art medical models under Apache 2.0 license. Models span 0.5B to 120B+ parameters, fine-tuned on clinical literature, case studies, and medical reasoning datasets. Excels at clinical summarization, differential diagnosis, patient triage, medical QA, treatment recommendations, and clinical documentation.
- **Base Model:** Various (multiple model families)
- **Relevance:** Very high. Massive collection of open medical models under permissive license.

---

## Multimodal Medical Models

### LLaVA-Med
- **GitHub:** https://github.com/microsoft/LLaVA-Med
- **Description:** Large Language and Vision Assistant for biomedicine by Microsoft. Trained using curriculum learning for adapting LLaVA to the biomedical domain. Supports open-ended biomedical visual question answering (VQA) on datasets like PathVQA and VQA-RAD. v1.5 released May 2024.
- **Base Model:** LLaVA (LLaMA-based vision-language model)
- **Relevance:** High. Leading multimodal medical AI for image-based clinical tasks.

### Visual Med-Alpaca
- **GitHub:** https://github.com/cambridgeltl/visual-med-alpaca
- **Description:** Open-source multimodal foundation model for the biomedical domain. Built on LLaMA-7B with plug-and-play visual modules. Can interpret radiological images and address complex clinical inquiries. Trainable on a single consumer GPU.
- **Base Model:** LLaMA-7B
- **Relevance:** Medium-high. Accessible multimodal medical model with low compute requirements.

---

## Medical Chatbots and QA Systems

### MedChat AI
- **GitHub:** https://github.com/HealthInnovators/MedChat-AI
- **Description:** Open-source LLM designed for healthcare chat applications. Provides accurate, reliable, and context-aware responses to medical information inquiries, health advice, and symptom analysis.
- **Base Model:** Custom/various
- **Relevance:** Medium. Focused healthcare chatbot framework.

### Doctor-Chatbot
- **GitHub:** https://github.com/LifestyleCorp/Doctor-Chatbot
- **Description:** Multimodal multi-agent LLM-powered open-source chatbot for diagnosing medical conditions, recommending physical examinations, advising investigations, and providing management plans.
- **Base Model:** Various LLMs
- **Relevance:** Medium-high. Multi-agent approach to clinical consultation.

### Llama2 Medical Chatbot
- **GitHub:** https://github.com/AIAnytime/Llama2-Medical-Chatbot
- **Description:** Medical bot built using Llama-2 and Sentence Transformers, powered by LangChain and Chainlit. Runs on CPU with minimum 16GB RAM.
- **Base Model:** Llama-2
- **Relevance:** Medium. Good template for LangChain-based medical chatbots.

### AI Medical Chatbot
- **GitHub:** https://github.com/ruslanmv/ai-medical-chatbot
- **Description:** Enterprise-grade conversational AI for medical consultation using IBM WatsonX, OpenAI GPT models, and RAG techniques.
- **Base Model:** IBM WatsonX / OpenAI GPT
- **Relevance:** Medium. Demonstrates enterprise medical chatbot architecture.

### HealifyAI
- **GitHub:** https://github.com/tanvir-ishraq/HealifyAI--LLM-based-Healthcare-System
- **Description:** Leverages multiple ML algorithms and LLMs to provide in-depth answers to medical queries and predicts conditions/diseases based on patient symptoms.
- **Base Model:** Multiple ML/LLM models
- **Relevance:** Medium. Combines traditional ML with LLMs for diagnosis.

---

## Medical RAG Systems

### Medical-RAG-LLM
- **GitHub:** https://github.com/AquibPy/Medical-RAG-LLM
- **Description:** Full-stack medical RAG system using BioMistral-7B as the main model, PubMedBERT for embeddings, Qdrant for vector DB, and LangChain + Llama CPP for orchestration. Complete open-source medical RAG pipeline.
- **Base Model:** BioMistral-7B + PubMedBERT embeddings
- **Relevance:** Very high. Reference implementation for medical RAG with open-source components.

### RAGFlow
- **GitHub:** https://github.com/infiniflow/ragflow
- **Description:** Leading open-source RAG engine that fuses RAG with agent capabilities. Not medical-specific but highly applicable to healthcare document processing and QA.
- **Base Model:** Model-agnostic (supports various LLMs)
- **Relevance:** Medium. General RAG framework applicable to medical use cases.

### Open Health
- **GitHub:** https://github.com/OpenHealthForAll/open-health
- **Description:** AI Health Assistant powered by user data. Supports Claude, GPT, and other models. Acts as an unbiased tool to guide users in managing long-term health.
- **Base Model:** Claude, GPT, and others (multi-model)
- **Relevance:** High. Health-focused AI assistant with RAG capabilities and multi-model support.

---

## Agentic Medical AI Frameworks

### Open Medicine
- **GitHub:** https://github.com/RamosFBC/openmedicine
- **Description:** Open-source Python library and MCP Server providing deterministic, DOI-traceable clinical reasoning for AI agents. Every calculator, score, and guideline returns its scientific source, forcing agents to rely on verified clinical standards. Pluggable into LangChain, AutoGPT, Claude Desktop, and other platforms.
- **Base Model:** Model-agnostic (provides tools for any LLM agent)
- **Relevance:** Very high. Evidence-based agentic clinical reasoning framework with MCP support.

### Multi-Agent Medical Assistant
- **GitHub:** https://github.com/souvikmajumder26/Multi-Agent-Medical-Assistant
- **Description:** GenAI-powered multi-agentic medical diagnostics and healthcare research chatbot. Features multi-agent orchestration with structured graph workflows, advanced RAG, confidence-based routing, and agent-to-agent handoff.
- **Base Model:** Various (multi-agent architecture)
- **Relevance:** Very high. Full multi-agent medical system with advanced orchestration.

### AI-Agents-for-Medical-Diagnostics
- **GitHub:** https://github.com/ahmadvh/AI-Agents-for-Medical-Diagnostics
- **Description:** Specialized LLM-based AI agents that analyze complex medical cases. Integrates insights from various medical professional roles to provide comprehensive assessments and personalized treatment recommendations.
- **Base Model:** Various LLMs
- **Relevance:** High. Multi-specialist agent approach to medical diagnostics.

### LLM-Medical-Agent
- **GitHub:** https://github.com/TUDB-Labs/LLM-Medical-Agent
- **Description:** Multi-agent framework for medical data processing.
- **Base Model:** Various
- **Relevance:** Medium-high. Framework-level approach to medical data agents.

### Healthcare-aigent
- **GitHub:** https://github.com/pkuppens/healthcare-aigent
- **Description:** Proof-of-concept AI system with modular multi-agent architecture supporting CrewAI and LangFlow. Designed to support healthcare professionals in patient communication and clinical documentation.
- **Base Model:** Various (supports multiple LLM providers)
- **Relevance:** Medium-high. Modular, framework-agnostic healthcare agent PoC.

### Agentic Healthcare AI
- **GitHub:** https://github.com/amitpuri/agentic-healthcare-ai
- **Description:** Healthcare AI agents demo with React frontend, FastAPI backend, FHIR API Gateway integration, and HIPAA-compliant security framework including encryption and access controls.
- **Base Model:** Various
- **Relevance:** High. Full-stack agentic healthcare system with FHIR and HIPAA compliance.

### HealthcareAgent
- **GitHub:** https://github.com/AI-Hub-Admin/HealthcareAgent
- **Description:** List of AI agents for healthcare and common agentic AI API interface definitions.
- **Base Model:** Various
- **Relevance:** Medium. Resource hub for healthcare agent APIs.

---

## Clinical Decision Support Tools

### Medical_LLM Pipeline (KatherLab)
- **GitHub:** https://github.com/KatherLab/Medical_LLM
- **Description:** Structured and meticulously designed pipeline for LLM-based medical projects. Provides a gateway to building clinical LLM applications with standardized workflows.
- **Base Model:** Various (pipeline framework)
- **Relevance:** Medium-high. Reusable pipeline for medical LLM projects.

### LLM Extractinator
- **GitHub:** https://github.com/DIAGNijmegen/llm_extractinator
- **Description:** Scalable, language-agnostic, open-source framework for automating data extraction tasks with LLMs in clinical and research settings.
- **Base Model:** Various LLMs
- **Relevance:** Medium. Useful for clinical data extraction pipelines.

---

## Biomedical NLP Foundation Models

### BioBERT
- **GitHub (code):** https://github.com/dmis-lab/biobert
- **GitHub (weights):** https://github.com/naver/biobert-pretrained
- **Description:** Pre-trained biomedical language representation model for biomedical text mining. Significantly outperforms general BERT on biomedical NER, relation extraction, and QA. Pre-trained on PubMed abstracts and PMC full-text articles.
- **Base Model:** BERT
- **Relevance:** High. Foundational biomedical NLP model widely used for downstream tasks.

### ClinicalBERT
- **GitHub:** https://github.com/EmilyAlsentzer/clinicalBERT
- **Description:** Publicly available clinical BERT embeddings trained on clinical notes. Presented at NAACL Clinical NLP Workshop 2019. Usable directly through the HuggingFace transformers library.
- **Base Model:** BERT (trained on MIMIC-III clinical notes)
- **Relevance:** High. Standard model for clinical NLP tasks.

### GatorTron
- **GitHub:** https://github.com/uf-hobi-informatics-lab/GatorTron
- **Hugging Face:** https://huggingface.co/UFNLP/gatortron-base
- **Description:** Largest clinical language model to date, developed by University of Florida and NVIDIA. Available in base (345M), medium (3.9B), and large (8.9B) parameter sizes. Designed for NER, relation extraction, and machine reading comprehension in clinical text.
- **Base Model:** BERT (Megatron implementation)
- **Relevance:** High. State-of-the-art clinical NLP encoder model at scale.

### BlueBERT
- **GitHub:** https://github.com/ncbi-nlp/bluebert
- **Description:** Pre-trained on PubMed abstracts and MIMIC-III clinical notes. Developed by NCBI/NLM. Available on HuggingFace.
- **Base Model:** BERT
- **Relevance:** Medium-high. Strong clinical + biomedical NLP model from NIH.

### SciBERT
- **GitHub:** https://github.com/allenai/scibert
- **Description:** BERT model pre-trained on scientific text (biomedicine and computer science) by Allen AI. Custom vocabulary trained from scratch on scientific corpus.
- **Base Model:** BERT
- **Relevance:** Medium. Broadly useful for scientific NLP including biomedical applications.

### PubMedBERT
- **Hugging Face:** https://huggingface.co/microsoft/BiomedNLP-PubMedBERT-base-uncased-abstract-fulltext
- **Description:** Domain-specific BERT model pre-trained from scratch on PubMed abstracts and full-text articles. Outperforms BioBERT on most biomedical NLP tasks due to domain-specific vocabulary.
- **Base Model:** BERT (trained from scratch on PubMed)
- **Relevance:** High. Often preferred over BioBERT for embedding and NLP tasks in medical RAG systems.

---

## MCP Servers and Claude/GPT-Based Health Tools

### Medical-MCP
- **GitHub:** https://github.com/JamesANZ/medical-mcp
- **Description:** MCP server providing comprehensive medical information by querying FDA, WHO, PubMed, Google Scholar, RxNorm, AAP, and pediatric journals. Integrates with Claude Desktop and Cursor.
- **Base Model:** Model-agnostic (MCP protocol)
- **Relevance:** Very high. Direct MCP integration for medical data access in Claude agents.

### Claude Ally-Health
- **GitHub:** https://github.com/huifer/Claude-Ally-Health
- **Also:** https://github.com/huifer/WellAlly-health
- **Description:** Intelligent healthcare assistant combining Claude AI with medical expertise. Supports symptom recording, medication management, medical record tracking, and multidisciplinary consultation via natural language.
- **Base Model:** Claude
- **Relevance:** High. Claude-native health assistant application.

---

## Benchmarks and Evaluation

### AgentClinic
- **GitHub:** https://github.com/SamuelSchmidgall/AgentClinic
- **Website:** https://agentclinic.github.io/
- **Description:** First open-source benchmark for evaluating LLMs as agents in simulated clinical environments. Includes AgentClinic-NEJM (multimodal) and AgentClinic-MedQA (dialogue). Supports 24 cognitive and implicit biases in doctor and patient agents. Supports HuggingFace, OpenAI, and Replicate models.
- **Base Model:** Model-agnostic (benchmark framework)
- **Relevance:** Very high. Essential for evaluating agentic medical AI systems.

### MedAgentBench
- **GitHub:** https://github.com/stanfordmlgroup/MedAgentBench
- **Description:** Stanford benchmark providing a realistic virtual EHR environment to benchmark medical LLM agents. Tests agent capabilities in electronic health record interactions.
- **Base Model:** Model-agnostic (benchmark)
- **Relevance:** Very high. EHR-focused agent evaluation from Stanford.

### Open Medical-LLM Leaderboard
- **Website:** https://huggingface.co/blog/leaderboard-medicalllm
- **Description:** HuggingFace leaderboard benchmarking LLMs in healthcare across standardized medical exams and clinical reasoning tasks.
- **Base Model:** N/A (leaderboard)
- **Relevance:** High. Central resource for comparing medical LLM performance.

---

## Curated Lists and Meta-Resources

### Awesome AI Agents for Healthcare
- **GitHub:** https://github.com/AgenticHealthAI/Awesome-AI-Agents-for-Healthcare
- **Description:** Curated list of research papers, projects, and resources on agentic AI and AI agents for healthcare, covering medical imaging, EHR, counseling, drug discovery, patient dialogue, and administration.
- **Relevance:** Very high. Comprehensive directory of healthcare AI agents.

### Awesome Medical Large Language Models
- **GitHub:** https://github.com/burglarhobbit/Awesome-Medical-Large-Language-Models
- **Description:** Curated papers on LLMs in healthcare and medical domains.
- **Relevance:** High. Academic reference collection.

### Awesome Specialized Medical LLMs
- **GitHub:** https://github.com/FreedomIntelligence/Awesome-Specialized-Medical-LLMs
- **Description:** Collection of research on specialized medical LLMs for specific diseases and medical specialties, organized by ICD-10 chapters.
- **Relevance:** High. Disease-specific and specialty-specific medical LLM directory.

### MedLLMs Practical Guide
- **GitHub:** https://github.com/AI-in-Health/MedLLMsPracticalGuide
- **Description:** Published in Nature Reviews Bioengineering. Curated list of practical guide resources including Medical LLMs Tree, comparison tables, and papers.
- **Relevance:** High. Authoritative academic guide to medical LLMs.

### LLM-for-Healthcare
- **GitHub:** https://github.com/KaiHe-better/LLM-for-Healthcare
- **Description:** Collection and tracking of existing and upcoming LLM tools and papers for healthcare and medicine.
- **Relevance:** Medium. Ongoing tracking resource.

### 500 AI Agents Projects
- **GitHub:** https://github.com/ashishpatel26/500-AI-Agents-Projects
- **Description:** Curated collection of 500 AI agent use cases across industries including healthcare, with links to open-source implementations.
- **Relevance:** Medium. Broader AI agents collection with healthcare section.

---

## Summary Statistics

| Category | Count |
|----------|-------|
| Medical LLMs | 11 |
| Multimodal Medical Models | 2 |
| Medical Chatbots/QA | 5 |
| Medical RAG Systems | 3 |
| Agentic Frameworks | 7 |
| Clinical Decision Support | 2 |
| Biomedical NLP Models | 6 |
| MCP/Claude/GPT Tools | 2 |
| Benchmarks | 3 |
| Curated Lists | 6 |
| **Total** | **47** |
