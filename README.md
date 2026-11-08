# SLM
Datasets

All datasets are public and are downloaded automatically by the code from the Hugging Face Hub:

Dataset	Use	Source
HotpotQA (distractor)	Main test (2,000 dev questions) and training	hotpotqa/hotpot_qa
Natural Questions Open	Questions and short answers	google-research-datasets/nq_open
BEIR Natural Questions	Wikipedia passages and relevance labels	mteb/nq
PubMedQA	Out-of-domain test and extra abstracts

notebooks/

Each notebook writes the package to disk, runs the tests, and then runs one step of the study on a Kaggle T4.

Notebook	What it runs
SLM_RAG_Step1_Kaggle.ipynb	Corrected measurement pipeline (prompting, answer extraction, scoring) and first runs
SLM_RAG_Step2_Kaggle.ipynb	Retrievers, 200,000-passage pool, context controls, PubMedQA
SLM_RAG_Step3_Kaggle.ipynb	Number of passages, passage order, prompts, other model families
SLM_RAG_Step4_Kaggle.ipynb	LoRA recipes (gold, noise, RAFT), capture after fine-tuning, confidence gate
SLM_RAG_Step5_Kaggle.ipynb	Repeated trainings (seeds) and PubMedQA transfer
SLM_RAG_Step6_Kaggle.ipynb	Natural Questions and SmolLM2-1.7B
SLM_RAG_Step7_Kaggle.ipynb	Training seeds 43/44, 200,000-passage NQ pool, NQ-trained adapters
SLM_RAG_Step7b_Kaggle.ipynb	The remaining NQ-trained adapter (Qwen2.5-1.5B, gold)
SLM_RAG_Step8_Kaggle.ipynb	NQ-trained adapters with seeds 43 and 44
