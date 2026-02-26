# Open-Source Bioinformatics & Genomics Tools for Individuals

Research compiled for the Agentic Health project. Last updated: 2026-02-26.

---

## 1. Personal Genomics Analysis Tools (23andMe / AncestryDNA Raw Data)

### OpenCRAVAT
- **URL:** https://opencravat.org / https://github.com/KarchinLab/open-cravat
- **Description:** Open-source Python framework for genomic variant interpretation, annotation, and scoring. Modular architecture with 300+ analysis modules. Accepts input from VCF files, HGVS strings, and personal genomics results from 23andMe or AncestryDNA. Processes ~1M variants/hour. Developed by Karchin Lab at Johns Hopkins University.
- **Relevance:** Directly accepts consumer genomics data and provides variant-level interpretation with a web GUI and local install options. Highly relevant for agents processing raw DTC genomic files.

### OSGenome
- **URL:** https://github.com/mentatpsi/OSGenome
- **Description:** Open-source web application for genetic data (SNPs) using 23andMe data. Stores and processes data locally -- nothing is sent externally. Relies on SNPedia data (110,000+ SNPs).
- **Relevance:** Local-first, privacy-preserving personal genomics analysis. Good for individuals who want to explore their SNP data without cloud uploads.

### Genetic Genie (GenVue Discovery)
- **URL:** https://geneticgenie.org/
- **Description:** Free tool for analyzing genomic data from 23andMe, AncestryDNA, and other DTC services. Provides methylation and detox reports. GenVue Discovery is positioned as a free Promethease alternative focused on health-related variants.
- **Relevance:** Free, accessible entry point for individuals wanting health-related genetic analysis from consumer raw data.

### openSNP
- **URL:** https://opensnp.org/ / https://github.com/openSNP/snpr
- **Description:** Open-source, non-profit platform that allows users to upload and share DTC genotype test results. Parses and annotates data, links to primary literature on variations.
- **Relevance:** Community-driven platform for open sharing and exploration of personal genetic data. Useful for citizen science and collaborative research.

### The Modern Promethease
- **URL:** https://github.com/ThomasKAtkins/TheModernPromethease
- **Description:** Open-source tool to create genomic reports based on 23andMe data. Built as an open alternative to the commercial Promethease service.
- **Relevance:** Open-source reimplementation of a popular commercial genetics report tool. Note: the author has expressed reservations about SNPedia data quality.

### Codegen.eu
- **URL:** https://codegen.eu/
- **Description:** Free comprehensive genetic report service. Accepts raw DNA data from consumer testing and provides technical health explanations linked to clinical studies. Currently being rebuilt.
- **Relevance:** Free alternative for genetic health reporting, though availability may be intermittent.

---

## 2. Variant Calling and Interpretation Tools

### GATK (Genome Analysis Toolkit)
- **URL:** https://gatk.broadinstitute.org/
- **Description:** Industry-standard open-source toolkit for identifying SNPs and indels in germline DNA and RNA-seq data. GATK4 includes Best Practices workflows for variant calling in gene panels, exomes, and whole genomes. Developed by the Broad Institute.
- **Relevance:** Gold standard for variant calling. More suited to technically proficient users or agent-driven pipelines, but essential infrastructure for any genomics workflow.

### DeepVariant
- **URL:** https://github.com/google/deepvariant
- **Description:** Open-source deep learning variant caller from Google Health. Uses convolutional neural networks to analyze pileup images of aligned reads. Produces filtered variants directly without post-calling refinement.
- **Relevance:** AI-powered, highly accurate variant caller. Suitable for automated agent pipelines processing sequencing data.

### OVarFlow
- **URL:** https://github.com/SebastianHollworksATcnag/OVarFlow
- **Description:** Resource-optimized, GATK4-based open-source variant calling workflow. Highly automated and reproducible, requiring minimal user interaction.
- **Relevance:** Designed for ease-of-use and automation -- good candidate for agent-driven variant calling with minimal human intervention.

### FreeBayes
- **URL:** https://github.com/freebayes/freebayes
- **Description:** Bayesian genetic variant detector designed to find small polymorphisms (SNPs, indels, MNPs, and complex events) from short-read sequencing data.
- **Relevance:** Lightweight, open-source alternative to GATK for variant calling.

### ANNOVAR
- **URL:** https://annovar.openbioinformatics.org/
- **Description:** Efficient tool for functional annotation of genetic variants detected from diverse genomes. Annotates variants with information from databases like ClinVar, dbSNP, ExAC.
- **Relevance:** Essential for interpreting what variants mean clinically and functionally. Bridges the gap between raw variant calls and actionable information.

### VEP (Variant Effect Predictor)
- **URL:** https://www.ensembl.org/vep
- **Description:** Ensembl's tool for determining the effect of variants on genes, transcripts, and protein sequence. Integrates with multiple annotation databases.
- **Relevance:** Widely used, well-maintained variant interpretation tool from EMBL-EBI. Critical for translating variant data into biological meaning.

---

## 3. Pharmacogenomics Tools

### PharmCAT (Pharmacogenomics Clinical Annotation Tool)
- **URL:** https://pharmcat.clinpgx.org/ / https://github.com/PharmGKB/PharmCAT
- **Description:** Open-source tool that takes individual genetic data (VCF files), identifies pharmacogenomic genotypes, infers haplotypes, predicts PGx phenotypes, and reports drug-prescribing recommendations from CPIC guidelines, DPWG guidelines, and FDA-approved drug labels.
- **Relevance:** Highly relevant for agentic health applications -- directly translates an individual's genetic data into actionable drug response predictions and dosing recommendations.

### PharmGKB (Pharmacogenomics Knowledge Base)
- **URL:** https://www.pharmgkb.org/
- **Description:** Comprehensive curated resource on the impact of genetic variation on drug response. Contains dosing guidelines, drug labels, gene-drug associations, and genotype-phenotype relationships.
- **Relevance:** Essential knowledge base for any pharmacogenomics pipeline. Freely accessible data that agents can query for drug-gene interaction information.

### Virtual Pharmacist
- **URL:** https://github.com/nicolenoelle/VirtualPharmacist (related publication: PLOS One)
- **Description:** Web-based platform that accepts microarray SNP genotyping data, FASTQ, and VCF files as inputs and reports potential drug responses in terms of efficacy, dosage, and toxicity.
- **Relevance:** Integrates multiple input formats and provides consolidated pharmacogenomics output. Available on GitHub.

### PGxDB
- **URL:** https://pgx-db.org/
- **Description:** Interactive web platform for comprehensive pharmacogenomics research. Enables analysis across genetic and drug response data types for cell-based validations and translational treatment strategies.
- **Relevance:** Research-oriented pharmacogenomics database useful for deeper exploration of drug-gene relationships.

---

## 4. Open-Source Genetic Counseling Aids

### Pedixplorer
- **URL:** https://bioconductor.org/packages/Pedixplorer / https://github.com/LouisLeNezet/Pedixplorer
- **Description:** R/Bioconductor package for handling complex pedigrees. Modernized version of kinship2, with S4 objects and a Shiny application for designing and visualizing complex pedigrees.
- **Relevance:** Open-source tool for pedigree analysis and visualization, essential for family-based genetic risk assessment.

### PediDraw
- **URL:** https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1950791/
- **Description:** Online pedigree drawing tool enabling step-by-step input of family information on the web. Outputs pedigrees and tables for genetic counseling.
- **Relevance:** Free, accessible tool for creating family pedigrees used in genetic counseling workflows.

### FamGenix
- **URL:** https://famgenix.com/
- **Description:** Free for genetic counseling students. Features pedigree drawing with built-in medical ontology, mobile-friendly patient history collection, and auto-identification of high-risk patients based on NCCN and ACMG/NSGC guidelines.
- **Relevance:** Bridges pedigree creation and automated risk assessment. Free for students, though full commercial use may require licensing.

---

## 5. Microbiome Analysis Tools

### QIIME 2
- **URL:** https://qiime2.org/ / https://github.com/qiime2/qiime2
- **Description:** Open-source bioinformatics pipeline for performing microbiome analysis from raw DNA sequencing data. Supports amplicon and metagenomics workflows with extensive plugin ecosystem.
- **Relevance:** Leading open-source microbiome analysis platform. Could be integrated into agent workflows for processing personal microbiome sequencing data.

### mothur
- **URL:** https://www.mothur.org/ / https://github.com/mothur/mothur
- **Description:** Open-source software for microbiome data analysis. Currently the most cited bioinformatics tool for analyzing 16S rRNA gene sequences. Created by Patrick Schloss, University of Michigan.
- **Relevance:** Highly established and well-documented. Suitable for processing personal microbiome testing data.

### MicrobiomeAnalyst
- **URL:** https://www.microbiomeanalyst.ca/
- **Description:** Web-based platform for comprehensive statistical, functional, and integrative analysis of microbiome data. Includes self-paced omics training and AI assistant features.
- **Relevance:** Accessible web interface lowers the barrier for non-expert microbiome analysis. Good candidate for agent-assisted microbiome interpretation.

### microbiome R package
- **URL:** https://microbiome.github.io/tutorials/
- **Description:** R package providing tools for microbiome analysis with multiple example datasets. Focuses on amplicon sequencing data with comprehensive tutorials.
- **Relevance:** Scriptable, open-source toolkit that agents can use programmatically for microbiome data processing.

### Qiita
- **URL:** https://qiita.ucsd.edu/
- **Description:** Open-source microbiome storage and analysis resource. Scalable from laptop to supercomputer. Supports multi-omics data integration.
- **Relevance:** Full-stack open-source platform for microbiome data management and analysis.

### Microbiome Modeling Toolbox
- **URL:** https://github.com/opencobra/cobratoolbox (MATLAB-based)
- **Description:** Suite of MATLAB tools for building and analyzing microbe-microbe and personalized microbiome models. Generates, simulates, and interprets microbiome interactions using metagenomic data.
- **Relevance:** Enables personalized microbiome modeling from individual metagenomic data.

---

## 6. Proteomics & Metabolomics Analysis Tools

### OpenMS
- **URL:** https://openms.de/ / https://github.com/OpenMS/OpenMS
- **Description:** Comprehensive open-source tool suite with 180+ tools for proteomics and metabolomics data processing workflows. Includes UmetaFlow for untargeted metabolomics and TOPPView Lite for web-based mass spectrometry data visualization.
- **Relevance:** Industry-leading open-source platform for mass spectrometry data analysis. Suitable for processing personal proteomics/metabolomics data.

### MetaboAnalyst
- **URL:** https://www.metaboanalyst.ca/
- **Description:** Web-based platform for metabolomics data analysis with AI-assisted features. Offers self-paced omics data science training. Supports statistical analysis, pathway analysis, and biomarker discovery.
- **Relevance:** Accessible web interface for metabolomics analysis. Could be used by individuals or agents to interpret personal metabolomics data.

### xcms (R package)
- **URL:** https://bioconductor.org/packages/xcms
- **Description:** One of the most widely used tools for LC-MS data preprocessing. Community-driven, open-source R package with modular and interoperable design for metabolomics.
- **Relevance:** Core infrastructure for metabolomics data processing pipelines.

### Galaxy
- **URL:** https://galaxyproject.org/
- **Description:** Web-based scientific analysis platform used by tens of thousands of scientists for genomics, proteomics, metabolomics, and imaging. Focuses on accessibility and reproducibility.
- **Relevance:** Multi-omics platform that makes complex analyses accessible to non-experts through a graphical workflow interface.

---

## 7. AI-Powered Genomics Interpretation

### AlphaGenome
- **URL:** https://deepmind.google/blog/alphagenome-ai-for-better-understanding-the-genome/
- **Description:** Google DeepMind AI tool (released June 2025) that predicts how single variants or mutations in human DNA impact biological processes regulating genes. Provides comprehensive and accurate predictions of variant effects.
- **Relevance:** State-of-the-art AI for variant effect prediction. Relevant for interpreting individual genetic variants in a health context.

### Evo 2
- **URL:** https://github.com/ArcInstitute/evo2 / https://arcinstitute.org/news/evo2
- **Description:** Open-source machine learning model trained on DNA from 100,000+ species across the tree of life. Can model and design genetic code for all domains of life. Integrated with NVIDIA BioNeMo framework.
- **Relevance:** Large-scale open-source genomic foundation model. Useful for understanding evolutionary conservation and functional impact of genetic variants.

### DeepVariant (also listed under Variant Calling)
- **URL:** https://github.com/google/deepvariant
- **Description:** Google's open-source deep learning variant caller using CNNs on pileup images.
- **Relevance:** AI-powered variant calling that can be integrated into personal genomics pipelines.

### DEGU
- **URL:** Published February 2026 (see medicalxpress.com coverage)
- **Description:** AI tool that improves accuracy and efficiency of genomic predictions by distilling ensembles of deep neural networks into a single smaller model. Provides better predictions with explanations.
- **Relevance:** Newer AI approach for genomic prediction that balances accuracy with interpretability.

### GenomeOcean
- **URL:** Developed by Berkeley Lab and Northwestern University
- **Description:** AI-powered large language model designed to learn the "natural language" of genomes. Reads vast amounts of genomic sequences to uncover patterns and relationships within DNA.
- **Relevance:** Foundational genomics LLM that could power future personal genomics interpretation tools.

---

## 8. Genetics-to-Lifestyle Recommendation Tools

### Nutrigenomix
- **URL:** https://nutrigenomix.com/
- **Description:** Genetic testing platform for personalized nutrition recommendations. Uses SNP analysis to provide diet, exercise, and supplement guidance based on genetic profile.
- **Relevance:** Commercial but scientifically grounded nutrigenomics service. Model for what open-source alternatives could provide.

### Genetic Life Hacks
- **URL:** https://www.geneticlifehacks.com/
- **Description:** Educational resource that helps individuals understand their genetic raw data in the context of lifestyle, nutrition, and health optimization. Provides guides for analyzing raw data from 23andMe and AncestryDNA.
- **Relevance:** Bridges genetics and lifestyle recommendations with educational content. Useful reference for building agentic nutrigenomics tools.

### SelfDecode
- **URL:** https://selfdecode.com/
- **Description:** AI-powered platform that analyzes genetic data and provides personalized health recommendations including diet, supplements, and lifestyle changes.
- **Relevance:** Commercial but demonstrates the model of AI-driven genetics-to-lifestyle recommendations. Relevant as a benchmark for open-source alternatives.

> **Note:** Truly open-source nutrigenomics-to-lifestyle tools remain scarce. This is a gap that the Agentic Health project could potentially address by combining open pharmacogenomics databases (PharmGKB), polygenic risk scores, and nutritional science literature.

---

## 9. Impute.me and Similar Personal Genomics Projects

### Impute.me (Archived)
- **URL:** https://www.frontiersin.org/articles/10.3389/fgene.2020.00578/full (paper) / Previously at impute.me
- **Description:** Open-source, non-profit tool that processed DTC genotype data through imputation to expand coverage, then calculated polygenic risk scores for 1,859 GWAS traits and 634 UK Biobank traits. Included modules for drug response, height, and personality traits. Taken offline in July 2022.
- **Relevance:** Pioneering open-source personal PRS tool. Though offline, its code and approach serve as a model for successor projects. The gap it left is partially filled by PRScalc and pgsc_calc.

### PRScalc
- **URL:** https://episphere.github.io/prs / https://github.com/episphere/prs
- **Description:** Privacy-preserving in-browser polygenic risk score calculator. Runs entirely in the browser with no data leaving the user's device. Matches PGS Catalog entries with 23andMe genome data (600K-1.4M SNPs). Built with JavaScript/HTML/CSS under MIT license.
- **Relevance:** Highly relevant for Agentic Health -- privacy-first, open-source, runs locally, and uses validated scores from the PGS Catalog. No installation needed.

### Open Humans
- **URL:** https://www.openhumans.org/ / https://github.com/OpenHumans
- **Description:** Community platform enabling personal data collection across data streams (genomes, GPS, wearables, CGM). 11,500+ members, 40+ tools and activities. 501(c)(3) nonprofit. Supports citizen science, academic research, and patient-led projects.
- **Relevance:** Infrastructure platform for personal data aggregation and sharing. Enables individuals to connect genetic data with other health data streams for holistic analysis.

---

## 10. Open-Source Polygenic Risk Score Calculators

### pgsc_calc (PGS Catalog Calculator)
- **URL:** https://github.com/PGScatalog/pgsc_calc / https://pgsc-calc.readthedocs.io/
- **Description:** Nextflow pipeline for reproducible polygenic score calculation. Automates PGS downloads from the PGS Catalog, variant matching, and parallel calculation of multiple PGS. Supports genetic ancestry estimation and score normalization. Scales from laptops to HPC clusters and cloud. Apache License.
- **Relevance:** The most comprehensive and well-maintained open-source PRS calculator. Essential tool for any agentic genomics pipeline.

### PGS Catalog
- **URL:** https://www.pgscatalog.org/
- **Description:** Open database of published polygenic scores and the metadata needed for accurate application and evaluation. Provides standardized scoring files and performance metrics.
- **Relevance:** Foundational open resource that PRS calculators (PRScalc, pgsc_calc) rely on. Contains thousands of validated polygenic scores.

### PRScalc (also listed above)
- **URL:** https://github.com/episphere/prs
- **Description:** In-browser PRS calculator using PGS Catalog data with 23andMe files. Privacy-preserving, no server upload required.
- **Relevance:** Lightweight, accessible PRS calculator for individuals with DTC genomics data.

### Polygenic Risk Score Knowledge Base
- **URL:** https://www.nature.com/articles/s42003-022-03795-x
- **Description:** Centralized online repository for calculating and contextualizing polygenic risk scores. Provides tools for PRS calculation and population-level contextualization.
- **Relevance:** Research resource for understanding and contextualizing PRS results.

---

## Curated Resource Lists

### awesome-genetics
- **URL:** https://github.com/plashchynski/awesome-genetics
- **Description:** Curated list of personal genomics software, libraries, and educational resources on GitHub. Includes tools like Codegen, Genomelink, and lineage (Python library for genetic genealogy).
- **Relevance:** Meta-resource for discovering additional personal genomics tools.

### Awesome-Bioinformatics
- **URL:** https://github.com/danielecook/Awesome-Bioinformatics
- **Description:** Curated list of bioinformatics libraries and software covering genome assembly, variant calling, visualization, and analysis.
- **Relevance:** Comprehensive index of bioinformatics tools for building analysis pipelines.

### Microbiome_notes
- **URL:** https://github.com/mdozmorov/Microbiome_notes
- **Description:** Continually expanding collection of microbiome analysis tools and resources.
- **Relevance:** Discovery resource for microbiome-specific tools.

### ISOGG Raw DNA Data Tools
- **URL:** https://isogg.org/wiki/Raw_DNA_data_tools
- **Description:** Community-maintained wiki listing tools for analyzing raw DNA data from consumer testing services.
- **Relevance:** Comprehensive directory of DTC genomics analysis tools maintained by the genetic genealogy community.

---

## Summary of Key Gaps and Opportunities for Agentic Health

1. **Nutrigenomics-to-Lifestyle:** No robust open-source tool currently translates genetic data into personalized nutrition and lifestyle recommendations. This is a clear opportunity.

2. **Unified Personal Genomics Agent:** Tools exist in silos (variant calling, PRS, pharmacogenomics, microbiome). An agent that orchestrates across these tools would be valuable.

3. **Privacy-Preserving Local Analysis:** PRScalc and OSGenome demonstrate the browser/local-first approach. More tools should follow this pattern for health data.

4. **Impute.me Successor:** The gap left by impute.me's shutdown (comprehensive imputation + PRS for DTC data) has not been fully filled. PRScalc covers PRS but lacks imputation.

5. **AI-Assisted Interpretation:** While AlphaGenome and Evo 2 are powerful, there is no open-source tool that combines AI interpretation with consumer-friendly output for personal health insights.

6. **Genetic Counseling Automation:** Open-source genetic counseling aids are limited to pedigree tools. AI-assisted pre-counseling triage and risk communication tools are missing.
