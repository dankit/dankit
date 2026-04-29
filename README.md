<p align="center"><strong>Modern applied AI/ML</strong><br/><sub>Projects grounded in practicality for today's world— multi-modal models, finetuning, agents, RAG, and other useful AI/ML tooling.</sub></p>


**[discord_sft_preview](https://github.com/dankit/discord_sft_preview)** *In progress* — Multi-turn **supervised fine-tuning** from raw, personal conversational data with focus on high-quality dialogue SFT. Uses Unsloth's training library for fused MoE kernels & LoRA on qwen3.5-35b-a3b, training based on model interpretability research papers & my own layer/module probing via gradient analysis, LoRA hotswap to vLLM for efficient inference and parallelized multi-modal evals, and more. This builds directly into: 
**[adversarial-agents-research-outline](https://github.com/dankit/adversarial-agents-research-outline)** · **computer use agents** to complete web tasks and captchas while mimicking plausible human behavior: Playwright harness, SFT & RL, gym environment, and my own data designer to turn manually collected seed data into high-quality synthetic data. 

**[Legal-RAG](https://github.com/dankit/Legal-RAG)** — Hosting models locally for embeddings and ranking, **Chroma** and **Elasticsearch**, **reciprocal rank fusion** for hybrid retrieval, agentic search, chatbot layer. Reranker finetuning on Google Cloud Platform (Kubernetes Engine and Compute Engine) with ephemeral/spot GPU considerations—[training infrastructure code](https://github.com/dankit/rag-reranker-finetuning). High performance on evals across the board: millions of embeddings and 250,000+ PDF pages from real-world data such as the US Code of Federal Regulations.

**[lambda_gpu_availability](https://github.com/dankit/lambda_gpu_availability)** — **Lambda Cloud** GPU capacity in near real time: stock, **alerts**, optional **auto-launch (“Snipe”)**, instance list/terminate—built because GPU availability was the main bottleneck for months.

**[LLM vram calculator](https://github.com/dankit/llm-vram-calc)** — Heavily vibe coded, but useful for telling if training or inference will OOM; contains interactive visuals showing the impact that different parameters have on vram: sequence length, batch size, gradient checkpointing, LoRA, optimizers, float precisions, and model weights. Refactor planned for the future.

<details>
<summary><strong>Foundations: applied ML theory & history (click here)</strong></summary>

I spent a long stretch going deep on **fundamentals**—math, classical ML, to modern deep learning—with **hands-on implementations**. The main idea was to apply what I learned from research papers along the way.

**[language-model-pretraining](https://github.com/dankit/language-model-pretraining)** — Roughly **450M-parameter** modern dense transformer, trained on the order of **10B tokens**; distributed data parallel on 8×A100 GPUs, my own training loops with checkpointing and model loading, PyTorch transformer implementation with SwiGLU, RMSNorm, Grouped Query Attention (GQA), RoPE, etc.

**[llama_3.1_8b_base_sft](https://github.com/dankit/llama_3.1_8b_base_sft)** — **Instruction tuning** the Llama 3.1 8B **base** checkpoint with **LoRA**, **quantization** exploration, complete with evals across the board (tinyMMLU, IFEval).

**[Attention is all you need](https://github.com/dankit/transformers)** — After classical ML theory, worked up to understanding and implementing the original transformers paper in PyTorch: sinusoidal positional encodings, LayerNorm, and different flavors of transformers (encoder-only, decoder-only, encoder-decoder). Some statistics learning for LayerNorm/RMSNorm; geometry/trigonometry for positional encodings, whether sinusoidal or eventually RoPE.

**[Classical ML](https://github.com/dankit/ML-learning)** — Classical ML before transformers: linear/logistic regression, linear algebra, calculus, shallow neural networks, loss functions, training loops, MNIST, etc. I understand surface-level concepts for CNNs, RNNs, LSTM, random forests, and more, but intentionally skipped deeper coverage to be time-efficient.

**Other** — The RAG project above touches on encoder-only transformers and their applications: from the original BERT model to variants (e.g. XLM-RoBERTa) for embeddings and reranking, plus how they're trained.

</details>
