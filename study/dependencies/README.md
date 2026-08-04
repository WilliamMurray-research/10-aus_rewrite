**10.1 - Data & Curriculum Strategy**

* 10.1.1 - Data Collection & Quality Filtering
* 10.1.2 - Deduplication Algorithms (MinHash, LSH) & Cleaning
* 10.1.3 - Data Structuring & Formatting
* 10.1.4 - High-Quality Synthetic Data Generation (Phi-Style "Textbooks")
* 10.1.5 - Data-Centric Curriculum Learning & Mixing Schedules
* 10.1.6 - Evaluation Dataset Creation

**10.2 - Architecture Design & Model Selection**

* 10.2.1 - Core Attention Variants (Encoder, Decoder, MQA, GQA, Cross-Attention)
* 10.2.2 - Linear Attention & Sub-Quadratic Architectures (SSMs, Mamba, RWKV, Hybrids)
* 10.2.3 - Sparse Architectures (Mixture of Experts / MoE for SLMs)
* 10.2.4 - Ultra-Low Precision Architectures (1-Bit, Ternary, Compressed Integer Architecture)
* 10.2.5 - Positional Encodings & Context Scaling (RoPE, YaRN, ALiBi)
* 10.2.6 - Model Initialisation, Scaling Laws & Compute-Optimal Frontiers
* 10.2.7 - Determinism & Small Model Stability Bounds

**10.3 - Pretraining & Tokenisation**

* 10.3.1 - Tokenisation & Vocabulary Compression (BPE, SentencePiece, Byte-Level)
* 10.3.2 - Embedding Representation & Weight Tying Techniques
* 10.3.3 - Distributed Pretraining Systems & Parallelism (Tensor, Pipeline, Zero-Redundancy)

**10.4 - Knowledge Distillation**

* 10.4.1 - Multi-Teacher & Cross-Architecture Distillation
* 10.4.2 - Logit Matching, Activation Matching & Feature Map Alignment
* 10.4.3 - Distillation Training Execution & Objective Functions

**10.5 - Post-Training, Fine-Tuning & Alignment**

* 10.5.1 - Supervised Fine-Tuning (SFT) & Instruction Tuning
* 10.5.2 - Parameter-Efficient Fine-Tuning (LoRA, QLoRA, DoRA, VeRA, Adapters)
* 10.5.3 - Preference Optimisation (RLHF, DPO, KTO, ORPO)
* 10.5.4 - Safety, Guardrails & Alignment Tuning

**10.6 - Evaluation, Benchmarking & Reliability**

* 10.6.1 - Automatic Benchmarks & Capabilities Testing
* 10.6.2 - Constrained Decoding Reliability (JSON, GBNF Grammars, Regex, Logit Masking)
* 10.6.3 - Function Calling & Micro-Agentic Tool Execution
* 10.6.4 - Human Evaluation & Red Teaming
* 10.6.5 - Regression Testing & Determinism Validation

**10.7 - Inference & Memory Optimisation**

* 10.7.1 - Quantisation Strategies (PTQ, QAT, AWQ, EXL2, GGUF Formats)
* 10.7.2 - KV Cache Optimisation (PagedAttention, FlashAttention, KV Compression/FP8)
* 10.7.3 - Speculative Decoding & Medusa-Style Head Acceleration
* 10.7.4 - Hardware-Aware Kernel Optimisation (Triton, CUDA, SIMD/AVX, ARM NEON/SVE)

**10.8 - Deployment & Edge Execution**

* 10.8.1 - Model Packaging, Export & Graph Optimization (ONNX, GGML/llama.cpp, TensorRT-LLM)
* 10.8.2 - Target-Specific Runtime Serving (Local Host GPUs, Edge, NPU, CPU Execution)
* 10.8.3 - Hardware Constraints (Roofline Model, Bandwidth Bottlenecks, Thermal/Power Envelope)
* 10.8.4 - Telemetry, Latency Jitter & Performance Monitoring

**10.9 - Experiment Tracking & Lab Management**

* 10.9.1 - Experiment Tracking & Hyperparameter Logging
* 10.9.2 - Dataset Versioning & Lineage
* 10.9.3 - Model Registry, Checkpoint Pruning & Lifecycle Management
