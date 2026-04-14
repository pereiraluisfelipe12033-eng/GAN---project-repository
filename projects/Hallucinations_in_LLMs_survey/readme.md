\# Controle de Alucinações em LLMs: Estudo Bibliográfico do Estado da Arte



\# Hallucination Control in LLMs: A State-of-the-Art Bibliographic Survey



\## Presentation



This project originated in the context of the graduate course \_IA376N - Generative AI: from models to multimodal applications\_,

offered in the first semester of 2026, at Unicamp, under the supervision of Prof. Dr. Paula Dornhofer Paro Costa, from the Department of Computer and Automation Engineering (DCA) of the School of Electrical and Computer Engineering (FEEC).



| Name | RA | Specialization |

|--|--|--|

| Charles Cavalcante Alcarde | `<RA>` | `<Electrical Engineering>` |

| Pedro Henrique Guerra | `<RA>` | `<Electrical Engineering>` |

| Luís Felipe da Silva Carlos Pereira | `<RA>` | `<Electrical Engineering>` |



\## Project Summary Description



Hallucination — the generation of fluent, syntactically correct text that is factually incorrect or entirely fabricated — is one of the central reliability challenges of Large Language Models (LLMs). As these models are increasingly deployed in high-stakes domains such as healthcare, law, finance, and education, understanding and mitigating hallucination becomes critical for safe real-world applications.



This project conducts a structured bibliographic survey of the state of the art in hallucination control in LLMs, covering the period from 2022 to 2025. The survey is organized around six axes: (1) taxonomy of hallucination types, (2) causes by pipeline phase, (3) detection techniques, (4) mitigation strategies, (5) evaluation benchmarks, and (6) open challenges and research directions.



A key distinction guiding this work is the separation between \*hallucination\* — fabricated information without grounding in context — and \*factuality\* — divergence from verifiable world facts. These are related but distinct phenomena requiring different mitigation strategies, a nuance frequently overlooked in the literature.



The primary output of this project is a comprehensive survey document synthesizing findings from over 300 identified mitigation studies. Depending on the group's progress, the survey may be extended with an experimental component evaluating one or more mitigation strategies on a controlled benchmark (such as HaluEval 2.0 or HalluLens), using open-source LLMs.



> 🎥 \*\*Proposal presentation video (max. 5 min.):\*\* `<link to be added upon recording>`



\## Proposed Methodology



\### Datasets and Benchmarks



The survey will analyze and compare the following datasets and benchmarks, selected to cover complementary dimensions of the problem:



\- \*\*TruthfulQA\*\* (Lin et al., 2022) — 817 adversarial questions across 38 categories. Widely used, though it measures factuality rather than hallucination proper.

\- \*\*HaluEval 2.0\*\* (2024) — 8,770 questions across five domains (biomedicine, finance, science, education, open domain). Primary candidate for any experimental extension.

\- \*\*FaithBench\*\* (2024) — human-annotated hallucinations in summaries from 10 modern LLMs across 8 model families.

\- \*\*HalluLens\*\* (Bang et al., 2025) — dynamic benchmark with continuous question generation to prevent benchmark leakage; rigorously distinguishes hallucination from factuality.

\- \*\*FACTSCORE / RAGAS\*\* (2023–2024) — decompose responses into individual claims for granular detection, scalable without human annotation.



\### Generative Modeling Approaches to be Studied



The survey maps six main categories of mitigation strategies:



1\. \*\*Training and learning\*\* — Supervised Fine-Tuning (SFT), RLHF, knowledge editing

2\. \*\*Architectural modifications\*\* — Retrieval-Augmented Generation (RAG), attention mechanisms

3\. \*\*Prompt and input optimization\*\* — Chain-of-Thought (CoT), self-consistency decoding, few-shot prompting

4\. \*\*Post-generation control\*\* — external fact-checking, LLM-as-a-judge, RAGAS

5\. \*\*Interpretability and diagnostics\*\* — uncertainty estimation, confidence calibration, internal state analysis (HalluShift)

6\. \*\*Agentic systems and orchestration\*\* — multi-agent pipelines, reflective RAG (DeepResearcher, FoRAG), self-refinement



\### Reference Articles



\- ALANSARI, A.; LUQMAN, H. Large Language Models Hallucination: A Comprehensive Survey. \*arXiv:2510.06265\*, 2025.

\- HUANG, L. et al. A Survey on Hallucination in LLMs: Principles, Taxonomy, Challenges. \*ACM Trans. Inf. Syst.\*, 2024.

\- From Illusion to Insight: A Taxonomic Survey of Hallucination Mitigation. \*MDPI AI Systems\*, 6(10), 2025.

\- Mitigating Hallucination in LLMs: RAG, Reasoning and Agentic Systems. \*arXiv:2510.24476\*, 2025.

\- ANH-HOANG et al. Survey and Analysis of Hallucinations: Attribution to Prompting or Model Behavior. \*Frontiers in AI\*, 2025.

\- BANG, Y. et al. HalluLens: LLM Hallucination Benchmark. \*arXiv:2504.17550\*, 2025.

\- FARQUHAR, S. et al. Detecting Hallucinations in Large Language Models Using Semantic Entropy. \*Nature\*, 2024.

\- WEI, J. et al. Chain-of-Thought Prompting Elicits Reasoning in Large Language Models. \*NeurIPS\*, 2022.

\- WANG, X. et al. Self-Consistency Improves Chain of Thought Reasoning in Language Models. \*ICLR\*, 2023.



\### Tools



\- Python + Jupyter / Google Colab for any experimental extension

\- Hugging Face Transformers and Datasets for model and benchmark access

\- RAGAS library for granular faithfulness evaluation

\- Zotero for bibliographic management

\- LaTeX / Markdown for the final survey document



\### Expected Results



\- A structured, self-contained survey document covering the six axes described above

\- A comparative taxonomy of mitigation strategies with analysis of trade-offs (computational cost, model modification requirement, applicability)

\- Identification and discussion of the RLHF alignment tax phenomenon as a central tension in the field

\- Critical analysis of benchmark limitations and the benchmark leakage problem

\- If the experimental extension is pursued: quantitative comparison of at least two mitigation approaches on HaluEval 2.0 using an open-source LLM



\### Evaluation Proposal



The survey itself will be evaluated through the quality, coverage, and critical depth of its bibliographic synthesis. For any experimental extension, evaluation will follow standard metrics for hallucination benchmarks: AUROC for detection tasks, accuracy and hallucination rate for generation tasks, using FACTSCORE or RAGAS for granular faithfulness scoring.



\## Schedule



| Stage | Description | Estimated Duration |

|--|--|--|

| E1 | Repository setup, proposal definition, initial bibliographic mapping | Weeks 1–2 |

| Bibliographic deepening | Full reading and synthesis of primary references across the six survey axes | Weeks 3–5 |

| Survey writing | Drafting the survey document: taxonomy, causes, detection, mitigation, benchmarks | Weeks 6–8 |

| E2 | Partial delivery: survey draft + progress report | TBD |

| Experimental extension (conditional) | Benchmark selection, model evaluation, results analysis | Weeks 9–10 |

| Final revision and integration | Survey finalization, figures, experimental results if applicable | Weeks 11–12 |

| E3 | Final delivery: complete survey + presentation | TBD |



\## Bibliographic References



\- ALANSARI, A.; LUQMAN, H. Large Language Models Hallucination: A Comprehensive Survey. \*arXiv:2510.06265\*, 2025.

\- HUANG, L. et al. A Survey on Hallucination in LLMs: Principles, Taxonomy, Challenges and Future Directions. \*ACM Transactions on Information Systems\*, 2024.

\- From Illusion to Insight: A Taxonomic Survey of Hallucination Mitigation Strategies in Large Language Models. \*MDPI AI Systems\*, 6(10), 2025.

\- Mitigating Hallucination in Large Language Models: RAG, Reasoning and Agentic Systems. \*arXiv:2510.24476\*, 2025.

\- ANH-HOANG et al. Survey and Analysis of Hallucinations in Large Language Models: Attribution to Prompting or Model Behavior. \*Frontiers in Artificial Intelligence\*, 2025.

\- BANG, Y. et al. HalluLens: LLM Hallucination Benchmark. \*arXiv:2504.17550\*, 2025.

\- FARQUHAR, S. et al. Detecting Hallucinations in Large Language Models Using Semantic Entropy. \*Nature\*, 630, 2024.

\- WEI, J. et al. Chain-of-Thought Prompting Elicits Reasoning in Large Language Models. \*NeurIPS\*, 2022.

\- WANG, X. et al. Self-Consistency Improves Chain of Thought Reasoning in Language Models. \*ICLR\*, 2023.

\- LIN, S. et al. TruthfulQA: Measuring How Models Mimic Human Falsehoods. \*ACL\*, 2022.



