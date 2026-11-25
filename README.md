# Awesome Private AI with stars

> Curated list of tools, frameworks, and resources for running, building, and deploying AI **privately** — on-prem, air-gapped, or self-hosted.

Private AI enables you to keep your data, models, and infrastructure **under your control**, avoiding unnecessary exposure to third parties. This list covers inference runtimes, model management, privacy tools, and more.

## **Contents**

* [Awesome Private AI  ](#awesome-private-ai--)
  * [**Contents**](#contents)
  * [Inference Runtimes & Backends](#inference-runtimes--backends)
  * [Model Management & Serving](#model-management--serving)
  * [Fine-Tuning & Adapters](#fine-tuning--adapters)
  * [Quantization & Compression](#quantization--compression)
  * [Vector Databases & Embeddings](#vector-databases--embeddings)
  * [Agents & Orchestration](#agents--orchestration)
  * [VS Code Plugins & Extensions](#vs-code-plugins--extensions)
  * [Privacy, Security & Governance](#privacy-security--governance)
  * [Observability & Evaluation](#observability--evaluation)
  * [Models for Private Deployment](#models-for-private-deployment)
  * [UI & Interaction Layers](#ui--interaction-layers)
  * [Image & Video Generation](#image--video-generation)
  * [Speech & Audio](#speech--audio)
  * [Datasets & Data Prep](#datasets--data-prep)
  * [Learning Resources & Research](#learning-resources--research)
  * [AI Routers & API Aggregators](#ai-routers--api-aggregators)
  * [Contributing](#contributing)
  * [License](#license)

## Inference Runtimes & Backends

> Engines and frameworks to run LLMs, vision, and multimodal models locally.

* [llama.cpp](https://github.com/ggml-org/llama.cpp) ⭐ 136,165 | 🐛 2,646 | 🌐 C++ | 📅 2026-11-25 - Portable, CPU/GPU-friendly LLM inference, good for GPU + CPU hybrid inference.
* [vLLM](https://github.com/vllm-project/vllm) ⭐ 97,513 | 🐛 11,110 | 🌐 Python | 📅 2026-11-25 - High-throughput, low-latency inference engine for LLMs.
* [Cherry Studio](https://github.com/CherryHQ/cherry-studio) ⭐ 53,842 | 🐛 3,025 | 🌐 TypeScript | 📅 2026-11-25 - Powerful and customizable cross-platform desktop app for LLM inference with built in web search, RAG, MCP support, and a quick assistant hotkey to summon your LLM from anywhere. Supports a wide variety of providers and OpenAI compatible endpoints for local inference.
* [LocalAI](https://github.com/mudler/LocalAI) ⭐ 50,529 | 🐛 227 | 🌐 Go | 📅 2026-11-25 - Drop-in OpenAI-compatible API for local inference across text, image, audio, and embedding models, with no GPU required.
* [exo](https://github.com/exo-explore/exo) ⭐ 48,593 | 🐛 474 | 🌐 Python | 📅 2026-11-06 - Run your own AI cluster at home with everyday devices. Dynamic model partitioning across multiple devices like iPhones, Macs, and Linux machines.
* [sglang](https://github.com/sgl-project/sglang) ⭐ 39,030 | 🐛 7,340 | 🌐 Python | 📅 2026-11-25 - Fast serving engine for LLMs and vision-language models, with RadixAttention prefix caching and a structured generation language.
* [llamafile](https://github.com/Mozilla-Ocho/llamafile) ⭐ 26,716 | 🐛 209 | 🌐 C++ | 📅 2026-11-09 - Distribute and run an entire LLM as a single executable file that works across six operating systems, with no install step.
* [oMLX](https://github.com/jundot/omlx) ⭐ 23,921 | 🐛 451 | 🌐 Python | 📅 2026-11-24 - macOS-native MLX inference server with paged SSD KV caching and continuous batching. Serves LLM, VLM, embedding, and reranker models over OpenAI- and Anthropic-compatible endpoints for local coding agents on Apple Silicon.
* [MLC LLM](https://github.com/mlc-ai/mlc-llm) ⭐ 23,452 | 🐛 369 | 🌐 Python | 📅 2026-11-21 - Compiler and runtime that deploys LLMs natively to GPUs, phones, and browsers via machine learning compilation.
* [KTransformers](https://github.com/kvcache-ai/ktransformers) ⭐ 19,696 | 🐛 538 | 🌐 Python | 📅 2026-11-24 - Optimized framework for running very large MoE models on limited hardware via GPU/CPU offloading and kernel injection.
* [text-generation-inference](https://github.com/huggingface/text-generation-inference) ⚠️ Archived - Optimized serving stack from Hugging Face.
* [mlx-lm](https://github.com/ml-explore/mlx-lm) ⭐ 7,753 | 🐛 322 | 🌐 Python | 📅 2026-11-24 - Fast, Apple Silicon-optimized LLM inference engine for running models locally and privately.
* [llama-swap](https://github.com/mostlygeek/llama-swap) ⭐ 6,308 | 🐛 120 | 🌐 Go | 📅 2026-11-24 - Model swapping for llama.cpp (or any local OpenAPI compatible server).
* [ik\_llama.cpp](https://github.com/ikawrakow/ik_llama.cpp) ⭐ 3,425 | 🐛 120 | 🌐 C++ | 📅 2026-11-24 - Fork of llama.cpp with bleeding edge feature implementations and quantization improvements.
* [RamaLama](https://github.com/containers/ramalama) ⭐ 3,118 | 🐛 115 | 🌐 Python | 📅 2026-11-23 - Runs models as OCI containers, pulling from registries you control — a good fit for air-gapped and enterprise workflows.
* [exllama3](https://github.com/turboderp-org/exllamav3) ⭐ 1,864 | 🐛 108 | 🌐 Python | 📅 2026-11-24 - An optimized quantization and inference library for running LLMs locally on modern consumer-class GPUs. Use TabbyAPI for an API server.
* [tabbyAPI](https://github.com/theroyallab/tabbyAPI) ⭐ 1,534 | 🐛 47 | 🌐 Python | 📅 2026-11-24 - Official API server for running exllamav2 and exllamav3 models. Aims to be a friendly backend with high customizablity and an idiotmatic OAI compatible API for users.
* [YALS (Yet another llamacpp server)](https://github.com/theroyallab/YALS) ⭐ 100 | 🐛 4 | 🌐 TypeScript | 📅 2026-03-28 - TabbyAPI's sister project, adapted for llama.cpp and GGUF models. Built from the ground up using libllama instead of wrapping llama-server.
* [Jan](https://jan.ai/) - Privacy-first, offline AI assistant and LLM runtime for local, secure inference.
* [LM Studio](https://lmstudio.ai/) - Cross-platform desktop app for running local LLMs with an easy-to-use interface.
* [LLM-D](https://llm-d.ai/) - Privacy-first, distributed LLM inference engine for scalable, local deployments.
* [Ollama](https://ollama.com) - Local LLM runner with model packaging. Uses llama.cpp backend to serve cautious model defaults.
* [GPT4All](https://gpt4all.io) - Local desktop model runner.

## Model Management & Serving

> Tools for hosting, scaling, and versioning AI models privately.

* [Triton Inference Server](https://github.com/triton-inference-server/server) ⭐ 11,163 | 🐛 902 | 🌐 Python | 📅 2026-11-25 - NVIDIA's multi-framework inference server, supporting TensorRT, PyTorch, ONNX, and vLLM backends behind one endpoint.
* [Xinference](https://github.com/xorbitsai/inference) ⭐ 9,668 | 🐛 40 | 🌐 Python | 📅 2026-11-25 - Serve and manage LLM, embedding, rerank, image, and audio models in one self-hosted cluster with an OpenAI-compatible API.
* [Seldon Core](https://github.com/SeldonIO/seldon-core) ⭐ 4,781 | 🐛 395 | 🌐 Go | 📅 2026-03-23 - Kubernetes-native model deployment.
* [vLLM Production Stack](https://github.com/vllm-project/production-stack) ⭐ 2,733 | 🐛 310 | 🌐 Python | 📅 2026-11-07 - End-to-end stack for deploying vLLM in production, including orchestration, monitoring, autoscaling, and best practices for private LLM serving.
* [OME (Open Model Engine)](https://github.com/sgl-project/ome) ⭐ 529 | 🐛 126 | 🌐 Go | 📅 2026-11-25 - Unified, open-source engine for serving, managing, and scaling LLMs and multimodal models privately. Supports sglang, vLLM, and more.
* [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - Scalable Python model serving.
* [KServe](https://kserve.github.io/website/) - Serverless model inference on Kubernetes.
* [BentoML](https://www.bentoml.com/) - Model packaging & serving framework.

## Fine-Tuning & Adapters

> Private workflows for adapting models to your needs.

* [Unsloth](https://github.com/unslothai/unsloth) ⭐ 80,197 | 🐛 579 | 🌐 Python | 📅 2026-11-25 - Fine-tune and reinforcement-train LLMs 2x faster with substantially less VRAM, on a single local GPU.
* [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) ⭐ 76,264 | 🐛 1,257 | 🌐 Python | 📅 2026-11-24 - Unified fine-tuning for 100+ models with a web UI, covering SFT, DPO, PPO, and reward modelling on your own hardware.
* [PEFT](https://github.com/huggingface/peft) ⭐ 21,916 | 🐛 113 | 🌐 Python | 📅 2026-11-25 - Parameter-efficient fine-tuning.
* [TRL](https://github.com/huggingface/trl) ⭐ 19,817 | 🐛 293 | 🌐 Python | 📅 2026-11-24 - Hugging Face's library for SFT, DPO, GRPO, and reward-model training on top of transformers.
* [ms-swift](https://github.com/modelscope/ms-swift) ⭐ 16,163 | 🐛 582 | 🌐 Python | 📅 2026-11-25 - Training and deployment toolkit covering 500+ LLMs and 200+ multimodal models, from PEFT through to quantized export.
* [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) ⭐ 12,749 | 🐛 257 | 🌐 Python | 📅 2026-11-20 - YAML-driven post-training framework covering full fine-tunes, LoRA, QLoRA, and multi-GPU sharding.
* [torchtune](https://github.com/pytorch/torchtune) ⭐ 5,824 | 🐛 474 | 🌐 Python | 📅 2026-11-19 - Native PyTorch library for fine-tuning and experimenting with LLMs, with readable single-file recipes.
* [LoRA](https://arxiv.org/abs/2106.09685) - Low-rank adaptation technique.
* [QLoRA](https://arxiv.org/abs/2305.14314) - Memory-efficient LoRA on quantized models.

## Quantization & Compression

> Shrink models to fit the hardware you actually own.

* [bitsandbytes](https://github.com/bitsandbytes-foundation/bitsandbytes) ⭐ 8,550 | 🐛 142 | 🌐 Python | 📅 2026-11-25 - 8-bit and 4-bit quantization primitives that underpin QLoRA and much of the local fine-tuning ecosystem.
* [llm-compressor](https://github.com/vllm-project/llm-compressor) ⭐ 3,992 | 🐛 169 | 🌐 Python | 📅 2026-11-25 - Apply GPTQ, SmoothQuant, SparseGPT, and FP8/INT4 weight-activation quantization, exporting straight to vLLM.
* [GPTQModel](https://github.com/ModelCloud/GPTQModel) ⭐ 1,296 | 🐛 25 | 🌐 Python | 📅 2026-11-25 - Actively maintained GPTQ toolkit for producing and running 4-bit quantized models.

## Vector Databases & Embeddings

> Private semantic search & retrieval-augmented generation.

* [FAISS](https://github.com/facebookresearch/faiss) ⭐ 41,911 | 🐛 394 | 🌐 C++ | 📅 2026-11-24 - Facebook AI Similarity Search.
* [Qdrant](https://github.com/qdrant/qdrant) ⭐ 35,691 | 🐛 857 | 🌐 Rust | 📅 2026-11-24 - High-performance Vector Database and Vector Search Engine.
* [pgvector](https://github.com/pgvector/pgvector) ⭐ 23,807 | 🐛 19 | 🌐 C | 📅 2026-11-24 - Vector similarity search inside PostgreSQL, keeping embeddings in the database you already self-host.
* [LanceDB](https://github.com/lancedb/lancedb) ⭐ 11,979 | 🐛 656 | 🌐 Rust | 📅 2026-11-25 - Embedded, serverless vector database that stores vectors and metadata as files on your own disk or object store.
* [text-embeddings-inference](https://github.com/huggingface/text-embeddings-inference) ⭐ 5,129 | 🐛 200 | 🌐 Rust | 📅 2026-11-24 - Fast local serving for embedding and reranker models, so retrieval never leaves your network.
* [Milvus](https://milvus.io) - Scalable vector database.
* [Weaviate](https://weaviate.io) - Open-source semantic search engine.
* [Chroma](https://www.trychroma.com/) - Local-first vector database.

## Agents & Orchestration

> Frameworks for chaining private AI tools & agents.

* [Langflow](https://github.com/langflow-ai/langflow) ⭐ 156,916 | 🐛 1,347 | 🌐 Python | 📅 2026-11-25 - Visual workflow builder for creating and deploying AI-powered agents and workflows with built-in API servers.
* [MetaGPT](https://github.com/FoundationAgents/MetaGPT) ⭐ 71,471 | 🐛 172 | 🌐 Python | 📅 2026-01-21 - Multi-agent framework for building collaborative AI systems with role-based agents that can work together on complex tasks.
* [Goose](https://github.com/block/goose) ⭐ 56,960 | 🐛 506 | 🌐 Rust | 📅 2026-11-25 - Local, extensible agent that runs on your machine and works against any LLM backend, including Ollama and other self-hosted endpoints.
* [Flowise](https://github.com/FlowiseAI/Flowise) ⚠️ Archived - No-code LangChain UI.
* [Aider](https://github.com/Aider-AI/aider) ⭐ 50,247 | 🐛 1,995 | 🌐 Python | 📅 2026-05-22 - Terminal-based pair programming agent that edits code in your local git repo, with support for local models via Ollama and OpenAI-compatible servers.
* [dspy](https://github.com/stanfordnlp/dspy) ⭐ 39,214 | 🐛 838 | 🌐 Python | 📅 2026-11-24 - Modular, open-source agent framework for building composable, private LLM applications and workflows.
* [CUA](https://github.com/trycua/cua) ⭐ 32,874 | 🐛 1,594 | 🌐 Rust | 📅 2026-11-25 -  enables AI agents to control full operating systems in virtual containers and deploy them locally or to the cloud.
* [Crush](https://github.com/charmbracelet/crush) ⭐ 29,189 | 🐛 587 | 🌐 Go | 📅 2026-11-25 - Privacy-first, open-source agentic coding and automation platform for local AI workflows.
* [PydanticAI](https://github.com/pydantic/pydantic-ai) ⭐ 21,370 | 🐛 1,997 | 🌐 Python | 📅 2026-11-25 - Python agent framework by the Pydantic team, model-agnostic with Ollama support for local deployment.
* [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) ⭐ 17,284 | 🐛 665 | 🌐 Python | 📅 2026-03-04 - Open-source, privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
* [DeepCode](https://github.com/HKUDS/DeepCode) ⭐ 16,865 | 🐛 32 | 🌐 Python | 📅 2026-11-23 - Open agentic coding framework that turns papers and specs into working code (Paper2Code, Text2Web, Text2Backend), running against local Ollama or vLLM backends.
* [Trae Agent](https://github.com/bytedance/trae-agent) ⭐ 12,221 | 🐛 255 | 🌐 Python | 📅 2026-02-05 - Privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
* [Bytebot](https://github.com/bytebot-ai/bytebot) ⚠️ Archived - A desktop agent is an AI that has its own computer. Unlike browser-only agents or traditional RPA tools, Bytebot comes with a full virtual desktop.
* [Orkas](https://github.com/Orkas-AI/Orkas) ⭐ 9,586 | 🐛 22 | 🌐 JavaScript | 📅 2026-11-24 - Open-source, local-first desktop AI workforce whose Commander coordinates specialist agents through one chat; model calls can use a compatible local endpoint.
* [agentgateway](https://github.com/agentgateway/agentgateway) ⭐ 6,412 | 🐛 359 | 🌐 Rust | 📅 2026-11-24 - Gateway for managing and orchestrating AI agents with support for local deployment.
* [AG2](https://github.com/ag2ai/ag2) ⭐ 5,088 | 🐛 99 | 🌐 Python | 📅 2026-11-24 - Open-source operating system for agentic AI with native Ollama support for local model deployment and multi-agent collaboration.
* [Skales](https://github.com/skalesapp/skales) ⭐ 2,239 | 🐛 2 | 📅 2026-11-24 - Source-available (BSL 1.1) local-first desktop AI agent that runs fully on-device, offline via Ollama or with 15+ providers; your files never leave your machine, no cloud required.
* [MFS](https://github.com/zilliztech/mfs) ⭐ 160 | 🐛 4 | 🌐 Python | 📅 2026-07-31 - Exposes your code, docs, chat (Slack/Gmail/Jira), databases and object stores as one file-like, searchable namespace for agents (`ls`/`cat`/`grep` + semantic search); runs fully local with on-device ONNX embeddings on Milvus, no API key.
* [LangChain](https://www.langchain.com/) - Agent and LLM orchestration framework.
* [Haystack](https://haystack.deepset.ai) - End-to-end RAG pipelines.
* [LlamaIndex](https://www.llamaindex.ai) - Data framework for LLM apps.
* [Herdr](https://herdr.dev/) - Self-hosted runtime and terminal multiplexer for coding agents. Runs the agent CLIs on your own machine or a box you control, grouping them into workspaces you can detach from and reattach to over SSH.
* [OpenCode AI](https://opencode.ai/) - Open-source agentic coding platform for private, local, and secure AI-powered development workflows.

## VS Code Plugins & Extensions

> Privacy-first, open-source agentic coding plugins and extensions for VS Code and other editors.

* [cline](https://github.com/cline/cline) ⭐ 71,877 | 🐛 1,828 | 🌐 TypeScript | 📅 2026-11-23 - Privacy-first, open-source agentic coding platform for local AI workflows and automation (VS Code extension).
* [Continue](https://github.com/continuedev/continue) ⭐ 36,556 | 🐛 862 | 🌐 TypeScript | 📅 2026-11-24 - Open-source autocomplete and chat assistant for VS Code and JetBrains, configurable against Ollama, llama.cpp, vLLM, and other local endpoints.
* [Tabby](https://github.com/TabbyML/tabby) ⭐ 33,927 | 🐛 350 | 🌐 Rust | 📅 2026-06-30 - Self-hosted AI coding assistant with its own inference server, offering a private alternative to hosted completion services.
* [Roo Code](https://github.com/RooCodeInc/Roo-Code) ⚠️ Archived - Privacy-first, open-source agentic coding platform for secure, local AI development (VS Code extension).

## Privacy, Security & Governance

> Keep AI deployments secure and compliant.

* [Presidio](https://github.com/microsoft/presidio) ⭐ 12,042 | 🐛 329 | 🌐 Python | 📅 2026-11-24 - Detect and de-identify PII in text and images before it ever reaches a model.
* [garak](https://github.com/NVIDIA/garak) ⭐ 10,169 | 🐛 617 | 🌐 Python | 📅 2026-11-23 - LLM vulnerability scanner that probes local models for prompt injection, jailbreaks, and data leakage.
* [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) ⭐ 7,573 | 🐛 292 | 🌐 Python | 📅 2026-11-25 - Add programmable topical and safety rails to LLM applications, running alongside self-hosted models.
* [LLM Guard](https://github.com/protectai/llm-guard) ⚠️ Archived - Input and output scanning toolkit covering prompt injection, PII, toxicity, and secrets leakage.
* [Concrete](https://github.com/zama-ai/concrete) ⭐ 1,584 | 🐛 58 | 🌐 C++ | 📅 2025-12-19 - Fully homomorphic encryption for AI.
* [OpenFL](https://github.com/securefederatedai/openfl) ⭐ 845 | 🐛 84 | 🌐 Python | 📅 2026-08-25 - Federated learning framework.
* [BlindAI](https://github.com/mithril-security/blindai) ⭐ 513 | 🐛 6 | 🌐 Rust | 📅 2024-03-19 - Confidential AI inference using TEEs.
* [Flower](https://flower.dev) - Federated learning at scale.

## Observability & Evaluation

> Measure and monitor private deployments without shipping traces to a vendor.

* [Langfuse](https://github.com/langfuse/langfuse) ⭐ 37,807 | 🐛 1,219 | 🌐 TypeScript | 📅 2026-11-24 - Self-hostable LLM observability, tracing, prompt management, and evaluation.
* [promptfoo](https://github.com/promptfoo/promptfoo) ⭐ 27,644 | 🐛 1,039 | 🌐 TypeScript | 📅 2026-11-25 - Local-first evaluation and red-teaming for prompts and models, runnable entirely offline in CI.
* [DeepEval](https://github.com/confident-ai/deepeval) ⭐ 19,654 | 🐛 890 | 🌐 Python | 📅 2026-11-24 - Unit-testing framework for LLM outputs, with metrics that can run against locally hosted judge models.
* [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) ⭐ 14,535 | 🐛 1,404 | 🌐 Python | 📅 2026-11-04 - The standard harness for benchmarking language models, supporting local vLLM and Hugging Face backends.
* [Phoenix](https://github.com/Arize-ai/phoenix) ⭐ 12,408 | 🐛 1,303 | 🌐 Python | 📅 2026-11-25 - Self-hosted tracing, evaluation, and experiment tracking for LLM applications.
* [OrcaReplay](https://github.com/Continuum-AI-Corp/OrcaReplay) ⭐ 1,198 | 🐛 3 | 🌐 TypeScript | 📅 2026-10-01 - Records an agent at the HTTP boundary and serves the recording back, so a run reproduces with the model server switched off; traces are files in the project and nothing is uploaded.

## Models for Private Deployment

> Open-weight models and model libraries you can self-host.

* [LLaMA 3](https://ai.meta.com/llama/) - Meta’s open-weight language model.
* [Mistral 7B](https://mistral.ai/news/announcing-mistral-7b/) - Dense 7B parameter model.
* [Qwen 3](https://qwenlm.github.io/blog/qwen3/) - A wide variety of general and specialized models in both dense and "Mixture of Experts" formats.
* [Kimi K2](https://moonshotai.github.io/Kimi-K2/) - Mixture-of-Experts model with 32 billion activated parameters and 1 trillion total parameters.
* [Phi-4](https://huggingface.co/microsoft/phi-4) - Small, high-quality models from Microsoft.
* [Mixtral](https://mistral.ai/news/mixtral-of-experts/) - Mixture-of-experts model.
* [Falcon](https://falconllm.tii.ae) - Open-source model from TII.
* [Gemma3](https://deepmind.google/models/gemma/gemma-3/) - Open source model from Google.
* [MLX Community](https://huggingface.co/mlx-community) - Community-driven Hugging Face page for open MLX models, optimized for Apple Silicon and private deployment.
* [Bielik](https://huggingface.co/speakleash) - An open source project that provides data, tools and LLMs for the development of the Polish artificial intelligence landscape

## UI & Interaction Layers

> Self-hosted chat & AI frontends.

* [Open WebUI](https://github.com/open-webui/open-webui) ⭐ 159,465 | 🐛 207 | 🌐 Svelte | 📅 2026-11-25 - Commonly recommended Web UI frontend which features built in search, web scrape, RAG, and optional user authentication.
* [Lobe Chat](https://github.com/lobehub/lobe-chat) ⭐ 86,116 | 🐛 1,449 | 🌐 TypeScript | 📅 2026-11-25 - Modern self-hosted chat framework with plugin and multimodal support, deployable in one click against local backends.
* [text-generation-webui](https://github.com/oobabooga/text-generation-webui) ⭐ 47,743 | 🐛 869 | 🌐 Python | 📅 2026-08-17 - Long-standing Gradio web UI for local text generation, supporting llama.cpp, ExLlama, and transformers backends.
* [LibreChat](https://github.com/danny-avila/LibreChat) ⭐ 47,503 | 🐛 1,156 | 🌐 TypeScript | 📅 2026-11-25 - Enhanced web UI for LLMs.
* [SillyTavern](https://github.com/SillyTavern/SillyTavern) ⭐ 36,053 | 🐛 546 | 🌐 JavaScript | 📅 2026-11-22 - Self-hosted, highly customizable frontend for local models, with extensive character, prompt, and context management.
* [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) ⭐ 33,310 | 🐛 245 | 🌐 TypeScript | 📅 2024-08-03 - Open-source ChatGPT clone.
* [Screenpipe](https://github.com/screenpipe/screenpipe) ⭐ 22,534 | 🐛 19 | 🌐 Rust | 📅 2026-11-25 - Source-available screen/audio history with local search and MCP; supports local Whisper transcription and Ollama, while configured cloud AI, transcription, sync, or integrations can send context off-device.
* [AnythingLLM](https://anythingllm.com/) - Full-stack private LLM workspace.

## Image & Video Generation

> Run diffusion and video models on your own GPUs.

* [AUTOMATIC1111 Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) ⭐ 165,372 | 🐛 2,511 | 🌐 Python | 📅 2026-03-02 - The most widely deployed self-hosted Stable Diffusion interface, with a large extension ecosystem.
* [ComfyUI](https://github.com/comfyanonymous/ComfyUI) ⭐ 148,481 | 🐛 5,633 | 🌐 Python | 📅 2026-11-25 - Node-based interface and backend for diffusion models, running image, video, and audio pipelines entirely locally.
* [InvokeAI](https://github.com/invoke-ai/InvokeAI) ⭐ 29,157 | 🐛 317 | 🌐 TypeScript | 📅 2026-11-25 - Professional-grade local generative image toolkit with a unified canvas and workflow editor.

## Speech & Audio

> Private speech-to-text and text-to-speech.

* [Whisper](https://github.com/openai/whisper) ⭐ 113,443 | 🐛 187 | 🌐 Python | 📅 2026-08-31 - The original open-weight speech recognition model, runnable fully offline.
* [whisper.cpp](https://github.com/ggml-org/whisper.cpp) ⭐ 55,496 | 🐛 368 | 🌐 C++ | 📅 2026-11-24 - C++ port of OpenAI's Whisper automatic speech recognition model, optimized for local, CPU/GPU inference without internet connectivity.
* [WhisperX](https://github.com/m-bain/whisperX) ⭐ 25,657 | 🐛 227 | 🌐 Python | 📅 2026-11-21 - Whisper with word-level timestamps, speaker diarization, and much faster batched transcription.
* [F5-TTS](https://github.com/SWivid/F5-TTS) ⭐ 15,655 | 🐛 71 | 🌐 Python | 📅 2026-11-03 - Local text-to-speech with voice cloning from a short reference sample.
* [RealtimeSTT](https://github.com/KoljaB/RealtimeSTT) ⭐ 10,263 | 🐛 146 | 🌐 Python | 📅 2026-11-11 - Low-latency local speech-to-text with voice activity detection, for building private voice interfaces.
* [speaches](https://github.com/speaches-ai/speaches) ⭐ 3,781 | 🐛 188 | 🌐 Python | 📅 2026-11-25 - Self-hosted OpenAI-compatible server for transcription, translation, and speech generation.

## Datasets & Data Prep

> Create and manage private training corpora.

* [MinerU](https://github.com/opendatalab/MinerU) ⭐ 84,297 | 🐛 21 | 🌐 Python | 📅 2026-11-22 - High-quality PDF-to-Markdown and JSON extraction, including formulas and tables, for building private corpora.
* [Docling](https://github.com/docling-project/docling) ⭐ 70,996 | 🐛 1,055 | 🌐 Python | 📅 2026-11-24 - Parse PDF, DOCX, PPTX, and HTML into structured formats for RAG and training, running entirely on your own hardware.
* [Marker](https://github.com/datalab-to/marker) ⭐ 41,062 | 🐛 84 | 🌐 Python | 📅 2026-11-20 - Fast, accurate document-to-Markdown conversion across PDFs, images, and office formats.
* [Label Studio](https://github.com/HumanSignal/label-studio) ⭐ 28,761 | 🐛 989 | 🌐 TypeScript | 📅 2026-11-25 - Self-hosted data labelling platform for text, image, audio, and video annotation.
* [Unstructured](https://github.com/Unstructured-IO/unstructured) ⭐ 15,778 | 🐛 490 | 🌐 HTML | 📅 2026-11-24 - Ingestion and preprocessing library for turning messy documents into model-ready chunks.
* [Argilla](https://github.com/argilla-io/argilla) ⭐ 5,213 | 🐛 38 | 🌐 Python | 📅 2026-11-23 - Collaborative tool for curating, annotating, and quality-checking datasets for fine-tuning and evaluation.
* [OpenWebText](https://skylion007.github.io/OpenWebTextCorpus/) - Open dataset similar to GPT training data.
* [RedPajama](https://www.together.xyz/blog/redpajama) - Open LLM training dataset.

## Learning Resources & Research

> Guides, papers, and tutorials on private AI.

* [LLMs from Scratch](https://github.com/rasbt/LLMs-from-scratch) ⭐ 109,007 | 🐛 4 | 🌐 Jupyter Notebook | 📅 2026-11-25 - Build a GPT-style model step by step in PyTorch, on your own machine.
* [LLM Course](https://github.com/mlabonne/llm-course) ⭐ 85,215 | 🐛 92 | 📅 2026-02-05 - Roadmap and notebooks covering LLM fundamentals, fine-tuning, quantization, and deployment.
* [ML Engineering Open Book](https://github.com/stas00/ml-engineering) ⭐ 19,745 | 🐛 1 | 🌐 Python | 📅 2026-11-25 - Field-tested notes on training and serving large models: hardware, parallelism, throughput, and debugging.
* [Smol Course](https://github.com/huggingface/smol-course) ⭐ 6,803 | 🐛 99 | 🌐 Jupyter Notebook | 📅 2026-11-17 - Hugging Face's practical course on aligning and fine-tuning small models that fit on local hardware.

## AI Routers & API Aggregators

> Centralized routers and proxy layers for aggregating, governing, and securing your private AI stack. These tools simplify connections to multiple model servers, optimize LLM routing, and provide observability, security, and compliance.

* [LiteLLM](https://github.com/BerriAI/litellm) ⭐ 63,842 | 🐛 5,486 | 🌐 Python | 📅 2026-11-25 - Self-hosted proxy exposing 100+ model backends — including Ollama, vLLM, and any OpenAI-compatible server — behind one API, with keys, budgets, routing, and logging.
* [Bifrost](https://github.com/maximhq/bifrost) ⭐ 10,006 | 🐛 1,733 | 🌐 Go | 📅 2026-11-25 - Self-hosted, open-source AI gateway for multi-provider routing, failover, observability, guardrails, and budget controls.
* [Nexus](https://github.com/grafbase/nexus) ⭐ 441 | 🐛 28 | 🌐 Rust | 📅 2026-03-16 - Open-source AI router to aggregate Model Context Protocol (MCP) servers, intelligently route requests to the best LLMs, and provide security, governance, observability, and simplified architecture for private AI deployments. [Blog](https://nexusrouter.com/blog/introducing-nexus-the-open-source-ai-router)

## Contributing

Contributions welcome! See [Contributing](CONTRIBUTING.md)

## License

Under CC0-1.0 license. see [LICENSE](LICENSE)

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-11-25._
