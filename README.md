# Synthetic Data Generation and Evaluation Using Reasoning Models

```
This repository contains the implementation and evaluation framework from our research on optimizing Retrieval-Augmented Generation (RAG) systems for technical domains. Our toolkit addresses the unique challenges of precise information extraction from complex, domain-specific documents by introducing granular, token-aware evaluation metrics and a synthetic data generation pipeline.
```
### Key Features

- **Token-Aware Evaluation Metrics:**  
  Introduces novel metrics — **PrecisionΩ** and **Intersection-over-Union (IoU)** — that quantify the trade-offs between context preservation and information density at the token level.

- **Synthetic Data Generation:**  
  A reasoning-driven pipeline leveraging instruction-tuned large language models (LLMs) (including DeepSeek-R1, its distilled variants, and Phi-4) to generate context-anchored QA pairs with discontinuous reference spans across specialized corpora.

- **Domain-Specific Corpus Support:**  
  Tailored for three challenging domains:
  - **Finance:** SEC 10-K filings
  - **Biomedical:** PubMed abstracts
  - **Cybersecurity:** APT threat reports

- **Granular Chunking Strategies:**  
  Empirical insights on the impact of chunk size on performance, revealing that smaller chunks (less than 10 tokens) can boost precision by 31–42% while highlighting the recall trade-offs. The toolkit allows you to experiment with and optimize chunking strategies to suit your domain-specific requirements.

- **Reproducible Multi-Metric Analysis:**  
  An end-to-end pipeline for automated synthetic dataset generation and multi-metric evaluation, ensuring reproducible and transparent optimization of RAG architectures for precision-sensitive applications.

This work bridges the gap between generic RAG systems and enterprise-level requirements for precise information retrieval in technical domains. Whether you're tackling financial risk assessments, biomedical research, or cybersecurity threat analysis, our toolkit offers a flexible and robust platform to fine-tune your models for improved performance.

## Evaluation Results

### DeepSeek-R1 Results 
![deepseek-r1-results.png](images%2Fdeepseek-r1-results.png)

### Deepseek-R1-Distill-LLAMA-70B, Deepseek-R1-Distill-QWEN-32B and MICROSOFT/PHI-4 Results Using BGE-M3 embeddings
![bge-3-embeddings-results.png](images%2Fbge-3-embeddings-results.png)

### Deepseek-R1-Distill-LLAMA-70B, Deepseek-R1-Distill-QWEN-32B and MICROSOFT/PHI-4 Results Using Nomic embeddings
![nomic-embeddings-results.png](images%2Fnomic-embeddings-results.png)

### Deepseek-R1-Distill-LLAMA-70B, Deepseek-R1-Distill-QWEN-32B and MICROSOFT/PHI-4 Results Using All-MiniLM embeddings
![all-minilm-embeddings-results.png](images%2Fall-minilm-embeddings-results.png)
![all-minilm-embeddings-2-results.png](images%2Fall-minilm-embeddings-2-results.png)