# LLM Builder Kit 

This repository tracks my journey to mastering LLaMA model training and serving on Azure. It combines hands-on learning with real-world tools like DeepSpeed, Megatron-LM, Hugging Face, Azure HPC (SLURM), AKS, and Azure Lustre.

---

## Learning Roadmap

### Phase 1: Foundations of LLMs & AI Infrastructure
**Objective:** Understand LLaMA internals, transformers, tokenization, and training with PyTorch + Hugging Face.

**Outcomes:**
- Fine-tuned LLaMA-7B with QLoRA
- Built preprocessing pipelines for multilingual corpora

---

### Phase 2: Distributed Training at Scale
**Objective:** Scale training with DeepSpeed, Megatron-LM, SLURM, and Azure Managed Lustre.

**Outcomes:**
- Trained models across multiple GPUs/nodes
- Used Lustre for parallel dataset streaming

---

### Phase 3: LLM Inference & Serving
**Objective:** Optimize and deploy LLaMA for production inference.

**Outcomes:**
- Served quantized models via vLLM and AKS
- Benchmarked performance and resource usage

---

### Phase 4: Monitoring & MLOps
**Objective:** Operationalize the end-to-end LLM lifecycle.

**Outcomes:**
- CI/CD for model updates
- Monitoring with Prometheus + Grafana
- Azure ML model registry & pipeline orchestration

---

### Phase 5: Real-World Projects
**Objective:** Apply all skills to domain-specific use cases in research and enterprise.

**Projects:**
- Domain-adapted LLaMA training
- Secure multi-tenant cluster setup
- Azure-integrated GenAI pipelines

---

## LLaMA on Azure: Full Stack for Training, Serving, and MLOps

This stack represents all the essential tools and technologies used to master training and serving LLaMA models at scale on Azure — from development and infrastructure to MLOps and monitoring.

| **Layer**                | **Component**              | **Tools & Technologies**                                                                 |
|--------------------------|----------------------------|-------------------------------------------------------------------------------------------|
| **Development & Core**   | Language                   | Python 3.10+, Jupyter, VS Code Remote SSH                                                 |
|                          | Libraries                  | PyTorch, Hugging Face Transformers, PEFT, Datasets, Accelerate                           |
|                          | Experiment Tracking        | Weights & Biases (wandb), MLflow                                                          |
|                          | Tokenization               | Hugging Face Tokenizers, SentencePiece                                                    |
| **Training Stack**       | Distributed Training       | DeepSpeed, Megatron-LM, FSDP                                                              |
|                          | Optimization Techniques    | LoRA, QLoRA, ZeRO (v1, v2, v3), Mixed Precision (FP16/BF16)                               |
|                          | Scheduler & Job Mgmt       | SLURM (Azure HPC), Azure ML Pipelines, KubeFlow                                           |
|                          | Compute Infra              | Azure NDv5 (H100), ND A100 VMs, AKS GPU node pools                                        |
|                          | Storage (Training)         | Azure Managed Lustre (Parallel I/O), Azure Blob                                           |
| **Serving Stack**        | Local Inference            | `transformers.pipeline`, vLLM, text-generation-webui                                      |
|                          | High-Performance Serving   | vLLM, Hugging Face TGI, Triton Inference Server                                           |
|                          | Deployment Platforms       | AKS, Azure ML Endpoints, KubeRay                                                          |
|                          | Quantization               | GPTQ, BitsAndBytes, AWQ                                                                   |
| **Data & Processing**    | Dataset Sources            | Hugging Face Datasets, OSCAR, The Pile, Domain-specific corpora                           |
|                          | Formats & Pipelines        | Parquet, Apache Arrow, JSONL, WebDataset                                                  |
|                          | Storage (Raw & Processed)  | Azure Blob Storage, Lustre, Azure Files                                                   |
| **MLOps & Observability**| Model Registry             | Azure ML Registry, MLflow                                                                 |
|                          | CI/CD                      | GitHub Actions, Azure DevOps                                                              |
|                          | Monitoring & Logging       | Prometheus, Grafana, Azure Monitor, wandb                                                 |
|                          | Prompt Evaluation          | BLEU, ROUGE, Perplexity (PPL), lm-eval-harness                                            |
| **Bonus / Advanced**     | Tokenizer Training         | SentencePiece, HF Tokenizers                                                              |
|                          | Multi-Tenant Setup         | SLURM Partitions, Azure AD, Lustre Quotas                                                 |
|                          | Auto-scaling Inference     | AKS Horizontal Autoscaler, KEDA, GPU-based workload scaling                               |
|                          | Research Integration       | Integration with Azure AI Search, Semantic Kernel, SK Agent for GenAI search workflows    |

---

**Author:** Hamza El-Ghoujdami  
**Role:** AI Specialist @ Microsoft  
**Focus:** Empowering organizations to build and deploy LLMs with Azure AI
