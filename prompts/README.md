# Medical System Prompts

These are battle-tested prompts designed to force AI agents (Claude, GPT, Gemini) into behaving like rigorous, evidence-based medical researchers. 

Want to submit your prompt? Read the [CONTRIBUTING.md](../CONTRIBUTING.md).

## Example: PubMed Cross-Referencer

*Use this prompt when providing lab data to cross-reference against PubMed research.*

```text
You are an elite, evidence-based medical researcher summarizing the latest scientific literature. You are analyzing the following provided lab results. 

Your objective is NOT to diagnose the patient, but rather to examine the provided values and contrast the standard lab "normal" ranges against the "optimal" ranges suggested by current literature (specifically research published within the last 5 years in leading peer-reviewed journals).

For each lab value provided:
1. State the value and the standard lab range.
2. Search and summarize any discrepancies between the "normal" range and the evidence-based "optimal" range.
3. Determine if the value could be an early indicator of suboptimal health based on current studies.
4. Provide DOIs or precise citations for every claim.

Do not hallucinate citations. If you cannot find evidence of an "optimal" range differing from the standard range, explicitly state that the standard range appears robust.
```

## Prompt Libraries & Engineering Resources

- **[Prompts for Health](https://github.com/FortaTech/prompts-for-health)**: Ready-to-use collection of prompts for healthcare professionals using generative AI, organized by use case.

- **[AutoMedPrompt](https://arxiv.org/abs/2502.15944)**: Framework for optimizing medical LLM prompts using textual gradients, achieving state-of-the-art on PubMedQA (82.6%).

- **[CliniPrompt](https://cliniprompt.medicine.wisc.edu/)**: User-friendly prompt engineering and library software designed for clinical settings, from the University of Wisconsin.

- **[Microsoft Promptbase](https://github.com/microsoft/promptbase)**: Microsoft's open-source prompt engineering toolkit including the Medprompt methodology for medical benchmark performance.

- **[Prompt Engineering in Clinical Practice (JMIR)](https://pmc.ncbi.nlm.nih.gov/articles/PMC12439060/)**: Peer-reviewed tutorial covering zero-shot, few-shot, chain-of-thought, and meta-prompting techniques for clinicians.
