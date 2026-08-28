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

* [llama.cpp](https://github.com/ggml-org/llama.cpp) ⭐ 125,997 | 🐛 2,250 | 🌐 C++ | 📅 2026-08-28 - Portable, CPU/GPU-friendly LLM inference, good for GPU + CPU hybrid inference.
* [vLLM](https://github.com/vllm-project/vllm) ⭐ 90,264 | 🐛 7,101 | 🌐 Python | 📅 2026-08-28 - High-throughput, low-latency inference engine for LLMs.
* [Cherry Studio](https://github.com/CherryHQ/cherry-studio) ⭐ 51,169 | 🐛 1,452 | 🌐 TypeScript | 📅 2026-08-28 - Powerful and customizable cross-platform desktop app for LLM inference with built in web search, RAG, MCP support, and a quick assistant hotkey to summon your LLM from anywhere. Supports a wide variety of providers and OpenAI compatible endpoints for local inference.
* [LocalAI](https://github.com/mudler/LocalAI) ⭐ 48,713 | 🐛 223 | 🌐 Go | 📅 2026-08-27 - Drop-in OpenAI-compatible API for local inference across text, image, audio, and embedding models, with no GPU required.
* [exo](https://github.com/exo-explore/exo) ⭐ 47,103 | 🐛 348 | 🌐 Python | 📅 2026-08-25 - Run your own AI cluster at home with everyday devices. Dynamic model partitioning across multiple devices like iPhones, Macs, and Linux machines.
* [sglang](https://github.com/sgl-project/sglang) ⭐ 32,592 | 🐛 4,968 | 🌐 Python | 📅 2026-08-28 - Fast serving engine for LLMs and vision-language models, with RadixAttention prefix caching and a structured generation language.
* [llamafile](https://github.com/Mozilla-Ocho/llamafile) ⭐ 25,709 | 🐛 212 | 🌐 C++ | 📅 2026-08-26 - Distribute and run an entire LLM as a single executable file that works across six operating systems, with no install step.
* [MLC LLM](https://github.com/mlc-ai/mlc-llm) ⭐ 23,103 | 🐛 335 | 🌐 Python | 📅 2026-08-17 - Compiler and runtime that deploys LLMs natively to GPUs, phones, and browsers via machine learning compilation.
* [oMLX](https://github.com/jundot/omlx) ⭐ 20,844 | 🐛 1,177 | 🌐 Python | 📅 2026-08-27 - macOS-native MLX inference server with paged SSD KV caching and continuous batching. Serves LLM, VLM, embedding, and reranker models over OpenAI- and Anthropic-compatible endpoints for local coding agents on Apple Silicon.
* [KTransformers](https://github.com/kvcache-ai/ktransformers) ⭐ 19,317 | 🐛 508 | 🌐 Python | 📅 2026-08-27 - Optimized framework for running very large MoE models on limited hardware via GPU/CPU offloading and kernel injection.
* [text-generation-inference](https://github.com/huggingface/text-generation-inference) ⚠️ Archived - Optimized serving stack from Hugging Face.
* [mlx-lm](https://github.com/ml-explore/mlx-lm) ⭐ 6,813 | 🐛 250 | 🌐 Python | 📅 2026-08-27 - Fast, Apple Silicon-optimized LLM inference engine for running models locally and privately.
* [llama-swap](https://github.com/mostlygeek/llama-swap) ⭐ 5,491 | 🐛 92 | 🌐 Go | 📅 2026-08-28 - Model swapping for llama.cpp (or any local OpenAPI compatible server).
* [ik\_llama.cpp](https://github.com/ikawrakow/ik_llama.cpp) ⭐ 3,109 | 🐛 90 | 🌐 C++ | 📅 2026-08-27 - Fork of llama.cpp with bleeding edge feature implementations and quantization improvements.
* [RamaLama](https://github.com/containers/ramalama) ⭐ 3,022 | 🐛 111 | 🌐 Python | 📅 2026-08-24 - Runs models as OCI containers, pulling from registries you control — a good fit for air-gapped and enterprise workflows.
* [tabbyAPI](https://github.com/theroyallab/tabbyAPI) ⭐ 1,325 | 🐛 38 | 🌐 Python | 📅 2026-08-26 - Official API server for running exllamav2 and exllamav3 models. Aims to be a friendly backend with high customizablity and an idiotmatic OAI compatible API for users.
* [exllama3](https://github.com/turboderp-org/exllamav3) ⭐ 1,176 | 🐛 64 | 🌐 Python | 📅 2026-08-26 - An optimized quantization and inference library for running LLMs locally on modern consumer-class GPUs. Use TabbyAPI for an API server.
* [YALS (Yet another llamacpp server)](https://github.com/theroyallab/YALS) ⭐ 99 | 🐛 4 | 🌐 TypeScript | 📅 2026-03-28 - TabbyAPI's sister project, adapted for llama.cpp and GGUF models. Built from the ground up using libllama instead of wrapping llama-server.
* [Jan](https://jan.ai/) - Privacy-first, offline AI assistant and LLM runtime for local, secure inference.
* [LM Studio](https://lmstudio.ai/) - Cross-platform desktop app for running local LLMs with an easy-to-use interface.
* [LLM-D](https://llm-d.ai/) - Privacy-first, distributed LLM inference engine for scalable, local deployments.
* [Ollama](https://ollama.com) - Local LLM runner with model packaging. Uses llama.cpp backend to serve cautious model defaults.
* [GPT4All](https://gpt4all.io) - Local desktop model runner.

## Model Management & Serving

> Tools for hosting, scaling, and versioning AI models privately.

* [Triton Inference Server](https://github.com/triton-inference-server/server) ⭐ 10,947 | 🐛 887 | 🌐 Python | 📅 2026-08-28 - NVIDIA's multi-framework inference server, supporting TensorRT, PyTorch, ONNX, and vLLM backends behind one endpoint.
* [Xinference](https://github.com/xorbitsai/inference) ⭐ 9,528 | 🐛 43 | 🌐 Python | 📅 2026-08-28 - Serve and manage LLM, embedding, rerank, image, and audio models in one self-hosted cluster with an OpenAI-compatible API.
* [Seldon Core](https://github.com/SeldonIO/seldon-core) ⭐ 4,779 | 🐛 396 | 🌐 Go | 📅 2026-03-23 - Kubernetes-native model deployment.
* [vLLM Production Stack](https://github.com/vllm-project/production-stack) ⭐ 2,531 | 🐛 198 | 🌐 Python | 📅 2026-08-18 - End-to-end stack for deploying vLLM in production, including orchestration, monitoring, autoscaling, and best practices for private LLM serving.
* [OME (Open Model Engine)](https://github.com/sgl-project/ome) ⭐ 496 | 🐛 128 | 🌐 Go | 📅 2026-08-27 - Unified, open-source engine for serving, managing, and scaling LLMs and multimodal models privately. Supports sglang, vLLM, and more.
* [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - Scalable Python model serving.
* [KServe](https://kserve.github.io/website/) - Serverless model inference on Kubernetes.
* [BentoML](https://www.bentoml.com/) - Model packaging & serving framework.

## Fine-Tuning & Adapters

> Private workflows for adapting models to your needs.

* [Unsloth](https://github.com/unslothai/unsloth) ⭐ 75,004 | 🐛 1,383 | 🌐 Python | 📅 2026-08-28 - Fine-tune and reinforcement-train LLMs 2x faster with substantially less VRAM, on a single local GPU.
* [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) ⭐ 74,404 | 🐛 1,135 | 🌐 Python | 📅 2026-08-27 - Unified fine-tuning for 100+ models with a web UI, covering SFT, DPO, PPO, and reward modelling on your own hardware.
* [PEFT](https://github.com/huggingface/peft) ⭐ 21,599 | 🐛 72 | 🌐 Python | 📅 2026-08-27 - Parameter-efficient fine-tuning.
* [TRL](https://github.com/huggingface/trl) ⭐ 19,163 | 🐛 292 | 🌐 Python | 📅 2026-08-27 - Hugging Face's library for SFT, DPO, GRPO, and reward-model training on top of transformers.
* [ms-swift](https://github.com/modelscope/ms-swift) ⭐ 15,388 | 🐛 632 | 🌐 Python | 📅 2026-08-27 - Training and deployment toolkit covering 500+ LLMs and 200+ multimodal models, from PEFT through to quantized export.
* [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) ⭐ 12,413 | 🐛 274 | 🌐 Python | 📅 2026-08-28 - YAML-driven post-training framework covering full fine-tunes, LoRA, QLoRA, and multi-GPU sharding.
* [torchtune](https://github.com/pytorch/torchtune) ⭐ 5,802 | 🐛 457 | 🌐 Python | 📅 2026-08-27 - Native PyTorch library for fine-tuning and experimenting with LLMs, with readable single-file recipes.
* [LoRA](https://arxiv.org/abs/2106.09685) - Low-rank adaptation technique.
* [QLoRA](https://arxiv.org/abs/2305.14314) - Memory-efficient LoRA on quantized models.

## Quantization & Compression

> Shrink models to fit the hardware you actually own.

* [bitsandbytes](https://github.com/bitsandbytes-foundation/bitsandbytes) ⭐ 8,443 | 🐛 67 | 🌐 Python | 📅 2026-08-27 - 8-bit and 4-bit quantization primitives that underpin QLoRA and much of the local fine-tuning ecosystem.
* [llm-compressor](https://github.com/vllm-project/llm-compressor) ⭐ 3,734 | 🐛 139 | 🌐 Python | 📅 2026-08-28 - Apply GPTQ, SmoothQuant, SparseGPT, and FP8/INT4 weight-activation quantization, exporting straight to vLLM.
* [GPTQModel](https://github.com/ModelCloud/GPTQModel) ⭐ 1,247 | 🐛 42 | 🌐 Python | 📅 2026-08-27 - Actively maintained GPTQ toolkit for producing and running 4-bit quantized models.

## Vector Databases & Embeddings

> Private semantic search & retrieval-augmented generation.

* [FAISS](https://github.com/facebookresearch/faiss) ⭐ 40,813 | 🐛 279 | 🌐 C++ | 📅 2026-08-26 - Facebook AI Similarity Search.
* [Qdrant](https://github.com/qdrant/qdrant) ⭐ 34,233 | 🐛 711 | 🌐 Rust | 📅 2026-08-28 - High-performance Vector Database and Vector Search Engine.
* [pgvector](https://github.com/pgvector/pgvector) ⭐ 22,788 | 🐛 14 | 🌐 C | 📅 2026-08-20 - Vector similarity search inside PostgreSQL, keeping embeddings in the database you already self-host.
* [LanceDB](https://github.com/lancedb/lancedb) ⭐ 11,298 | 🐛 603 | 🌐 Rust | 📅 2026-08-28 - Embedded, serverless vector database that stores vectors and metadata as files on your own disk or object store.
* [text-embeddings-inference](https://github.com/huggingface/text-embeddings-inference) ⭐ 5,030 | 🐛 210 | 🌐 Rust | 📅 2026-07-24 - Fast local serving for embedding and reranker models, so retrieval never leaves your network.
* [Milvus](https://milvus.io) - Scalable vector database.
* [Weaviate](https://weaviate.io) - Open-source semantic search engine.
* [Chroma](https://www.trychroma.com/) - Local-first vector database.

## Agents & Orchestration

> Frameworks for chaining private AI tools & agents.

* [Langflow](https://github.com/langflow-ai/langflow) ⭐ 153,755 | 🐛 993 | 🌐 Python | 📅 2026-08-28 - Visual workflow builder for creating and deploying AI-powered agents and workflows with built-in API servers.
* [MetaGPT](https://github.com/FoundationAgents/MetaGPT) ⭐ 70,073 | 🐛 133 | 🌐 Python | 📅 2026-01-21 - Multi-agent framework for building collaborative AI systems with role-based agents that can work together on complex tasks.
* [Flowise](https://github.com/FlowiseAI/Flowise) ⚠️ Archived - No-code LangChain UI.
* [Goose](https://github.com/block/goose) ⭐ 53,589 | 🐛 222 | 🌐 Rust | 📅 2026-08-27 - Local, extensible agent that runs on your machine and works against any LLM backend, including Ollama and other self-hosted endpoints.
* [Aider](https://github.com/Aider-AI/aider) ⭐ 48,539 | 🐛 1,827 | 🌐 Python | 📅 2026-05-22 - Terminal-based pair programming agent that edits code in your local git repo, with support for local models via Ollama and OpenAI-compatible servers.
* [dspy](https://github.com/stanfordnlp/dspy) ⭐ 37,628 | 🐛 635 | 🌐 Python | 📅 2026-08-27 - Modular, open-source agent framework for building composable, private LLM applications and workflows.
* [Crush](https://github.com/charmbracelet/crush) ⭐ 27,745 | 🐛 681 | 🌐 Go | 📅 2026-08-27 - Privacy-first, open-source agentic coding and automation platform for local AI workflows.
* [CUA](https://github.com/trycua/cua) ⭐ 21,962 | 🐛 736 | 🌐 HTML | 📅 2026-08-28 -  enables AI agents to control full operating systems in virtual containers and deploy them locally or to the cloud.
* [PydanticAI](https://github.com/pydantic/pydantic-ai) ⭐ 19,542 | 🐛 750 | 🌐 Python | 📅 2026-08-28 - Python agent framework by the Pydantic team, model-agnostic with Ollama support for local deployment.
* [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) ⭐ 17,031 | 🐛 532 | 🌐 Python | 📅 2026-03-04 - Open-source, privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
* [DeepCode](https://github.com/HKUDS/DeepCode) ⭐ 16,438 | 🐛 26 | 🌐 Python | 📅 2026-08-27 - Open agentic coding framework that turns papers and specs into working code (Paper2Code, Text2Web, Text2Backend), running against local Ollama or vLLM backends.
* [Trae Agent](https://github.com/bytedance/trae-agent) ⭐ 12,058 | 🐛 159 | 🌐 Python | 📅 2026-02-05 - Privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
* [Bytebot](https://github.com/bytebot-ai/bytebot) ⚠️ Archived - A desktop agent is an AI that has its own computer. Unlike browser-only agents or traditional RPA tools, Bytebot comes with a full virtual desktop.
* [AG2](https://github.com/ag2ai/ag2) ⭐ 4,891 | 🐛 30 | 🌐 Python | 📅 2026-08-28 - Open-source operating system for agentic AI with native Ollama support for local model deployment and multi-agent collaboration.
* [agentgateway](https://github.com/agentgateway/agentgateway) ⭐ 4,610 | 🐛 249 | 🌐 Rust | 📅 2026-08-27 - Gateway for managing and orchestrating AI agents with support for local deployment.
* [Skales](https://github.com/skalesapp/skales) ⭐ 1,729 | 🐛 1 | 🌐 TypeScript | 📅 2026-08-27 - Source-available (BSL 1.1) local-first desktop AI agent that runs fully on-device, offline via Ollama or with 15+ providers; your files never leave your machine, no cloud required.
* [Orkas](https://github.com/Orkas-AI/Orkas) ⭐ 1,477 | 🐛 15 | 🌐 TypeScript | 📅 2026-08-28 - Open-source, local-first desktop AI workforce whose Commander coordinates specialist agents through one chat; model calls can use a compatible local endpoint.
* [MFS](https://github.com/zilliztech/mfs) ⭐ 129 | 🐛 3 | 🌐 Python | 📅 2026-07-31 - Exposes your code, docs, chat (Slack/Gmail/Jira), databases and object stores as one file-like, searchable namespace for agents (`ls`/`cat`/`grep` + semantic search); runs fully local with on-device ONNX embeddings on Milvus, no API key.
* [LangChain](https://www.langchain.com/) - Agent and LLM orchestration framework.
* [Haystack](https://haystack.deepset.ai) - End-to-end RAG pipelines.
* [LlamaIndex](https://www.llamaindex.ai) - Data framework for LLM apps.
* [Herdr](https://herdr.dev/) - Self-hosted runtime and terminal multiplexer for coding agents. Runs the agent CLIs on your own machine or a box you control, grouping them into workspaces you can detach from and reattach to over SSH.
* [OpenCode AI](https://opencode.ai/) - Open-source agentic coding platform for private, local, and secure AI-powered development workflows.

## VS Code Plugins & Extensions

> Privacy-first, open-source agentic coding plugins and extensions for VS Code and other editors.

* [cline](https://github.com/cline/cline) ⭐ 67,028 | 🐛 1,121 | 🌐 TypeScript | 📅 2026-08-28 - Privacy-first, open-source agentic coding platform for local AI workflows and automation (VS Code extension).
* [Continue](https://github.com/continuedev/continue) ⭐ 35,651 | 🐛 941 | 🌐 TypeScript | 📅 2026-08-27 - Open-source autocomplete and chat assistant for VS Code and JetBrains, configurable against Ollama, llama.cpp, vLLM, and other local endpoints.
* [Tabby](https://github.com/TabbyML/tabby) ⭐ 33,839 | 🐛 332 | 🌐 Rust | 📅 2026-06-30 - Self-hosted AI coding assistant with its own inference server, offering a private alternative to hosted completion services.
* [Roo Code](https://github.com/RooCodeInc/Roo-Code) ⚠️ Archived - Privacy-first, open-source agentic coding platform for secure, local AI development (VS Code extension).

## Privacy, Security & Governance

> Keep AI deployments secure and compliant.

* [Presidio](https://github.com/microsoft/presidio) ⭐ 10,659 | 🐛 106 | 🌐 Python | 📅 2026-08-26 - Detect and de-identify PII in text and images before it ever reaches a model.
* [garak](https://github.com/NVIDIA/garak) ⭐ 9,048 | 🐛 405 | 🌐 Python | 📅 2026-08-25 - LLM vulnerability scanner that probes local models for prompt injection, jailbreaks, and data leakage.
* [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) ⭐ 7,023 | 🐛 204 | 🌐 Python | 📅 2026-08-27 - Add programmable topical and safety rails to LLM applications, running alongside self-hosted models.
* [LLM Guard](https://github.com/protectai/llm-guard) ⚠️ Archived - Input and output scanning toolkit covering prompt injection, PII, toxicity, and secrets leakage.
* [Concrete](https://github.com/zama-ai/concrete) ⭐ 1,574 | 🐛 57 | 🌐 C++ | 📅 2025-12-19 - Fully homomorphic encryption for AI.
* [OpenFL](https://github.com/securefederatedai/openfl) ⭐ 842 | 🐛 83 | 🌐 Python | 📅 2026-08-25 - Federated learning framework.
* [BlindAI](https://github.com/mithril-security/blindai) ⭐ 512 | 🐛 6 | 🌐 Rust | 📅 2024-03-19 - Confidential AI inference using TEEs.
* [Flower](https://flower.dev) - Federated learning at scale.

## Observability & Evaluation

> Measure and monitor private deployments without shipping traces to a vendor.

* [Langfuse](https://github.com/langfuse/langfuse) ⭐ 33,829 | 🐛 832 | 🌐 TypeScript | 📅 2026-08-27 - Self-hostable LLM observability, tracing, prompt management, and evaluation.
* [promptfoo](https://github.com/promptfoo/promptfoo) ⭐ 24,626 | 🐛 535 | 🌐 TypeScript | 📅 2026-08-28 - Local-first evaluation and red-teaming for prompts and models, runnable entirely offline in CI.
* [DeepEval](https://github.com/confident-ai/deepeval) ⭐ 17,918 | 🐛 485 | 🌐 Python | 📅 2026-08-26 - Unit-testing framework for LLM outputs, with metrics that can run against locally hosted judge models.
* [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) ⭐ 13,815 | 🐛 922 | 🌐 Python | 📅 2026-08-27 - The standard harness for benchmarking language models, supporting local vLLM and Hugging Face backends.
* [Phoenix](https://github.com/Arize-ai/phoenix) ⭐ 11,220 | 🐛 925 | 🌐 Python | 📅 2026-08-28 - Self-hosted tracing, evaluation, and experiment tracking for LLM applications.

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

* [Open WebUI](https://github.com/open-webui/open-webui) ⭐ 150,170 | 🐛 214 | 🌐 Python | 📅 2026-08-27 - Commonly recommended Web UI frontend which features built in search, web scrape, RAG, and optional user authentication.
* [Lobe Chat](https://github.com/lobehub/lobe-chat) ⭐ 82,050 | 🐛 823 | 🌐 TypeScript | 📅 2026-08-28 - Modern self-hosted chat framework with plugin and multimodal support, deployable in one click against local backends.
* [text-generation-webui](https://github.com/oobabooga/text-generation-webui) ⭐ 47,589 | 🐛 840 | 🌐 Python | 📅 2026-08-17 - Long-standing Gradio web UI for local text generation, supporting llama.cpp, ExLlama, and transformers backends.
* [LibreChat](https://github.com/danny-avila/LibreChat) ⭐ 42,538 | 🐛 730 | 🌐 TypeScript | 📅 2026-08-28 - Enhanced web UI for LLMs.
* [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) ⭐ 33,340 | 🐛 240 | 🌐 TypeScript | 📅 2024-08-03 - Open-source ChatGPT clone.
* [SillyTavern](https://github.com/SillyTavern/SillyTavern) ⭐ 32,736 | 🐛 595 | 🌐 JavaScript | 📅 2026-08-26 - Self-hosted, highly customizable frontend for local models, with extensive character, prompt, and context management.
* [Screenpipe](https://github.com/screenpipe/screenpipe) ⭐ 21,265 | 🐛 89 | 🌐 Rust | 📅 2026-08-28 - 24/7 local screen + microphone recording with OCR, audio transcription, and semantic search. Fully offline with Ollama or any local LLM. MCP server for Claude.
* [AnythingLLM](https://anythingllm.com/) - Full-stack private LLM workspace.

## Image & Video Generation

> Run diffusion and video models on your own GPUs.

* [AUTOMATIC1111 Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) ⭐ 164,695 | 🐛 2,501 | 🌐 Python | 📅 2026-03-02 - The most widely deployed self-hosted Stable Diffusion interface, with a large extension ecosystem.
* [ComfyUI](https://github.com/comfyanonymous/ComfyUI) ⭐ 130,343 | 🐛 4,724 | 🌐 Python | 📅 2026-08-28 - Node-based interface and backend for diffusion models, running image, video, and audio pipelines entirely locally.
* [InvokeAI](https://github.com/invoke-ai/InvokeAI) ⭐ 28,026 | 🐛 384 | 🌐 Python | 📅 2026-08-27 - Professional-grade local generative image toolkit with a unified canvas and workflow editor.

## Speech & Audio

> Private speech-to-text and text-to-speech.

* [Whisper](https://github.com/openai/whisper) ⭐ 108,038 | 🐛 136 | 🌐 Python | 📅 2026-07-28 - The original open-weight speech recognition model, runnable fully offline.
* [whisper.cpp](https://github.com/ggml-org/whisper.cpp) ⭐ 53,239 | 🐛 1,240 | 🌐 C++ | 📅 2026-08-25 - C++ port of OpenAI's Whisper automatic speech recognition model, optimized for local, CPU/GPU inference without internet connectivity.
* [WhisperX](https://github.com/m-bain/whisperX) ⭐ 23,782 | 🐛 215 | 🌐 Python | 📅 2026-07-13 - Whisper with word-level timestamps, speaker diarization, and much faster batched transcription.
* [F5-TTS](https://github.com/SWivid/F5-TTS) ⭐ 15,170 | 🐛 60 | 🌐 Python | 📅 2026-07-23 - Local text-to-speech with voice cloning from a short reference sample.
* [RealtimeSTT](https://github.com/KoljaB/RealtimeSTT) ⭐ 10,082 | 🐛 147 | 🌐 Python | 📅 2026-08-27 - Low-latency local speech-to-text with voice activity detection, for building private voice interfaces.
* [speaches](https://github.com/speaches-ai/speaches) ⭐ 3,625 | 🐛 142 | 🌐 Python | 📅 2026-08-28 - Self-hosted OpenAI-compatible server for transcription, translation, and speech generation.

## Datasets & Data Prep

> Create and manage private training corpora.

* [MinerU](https://github.com/opendatalab/MinerU) ⭐ 78,647 | 🐛 103 | 🌐 Python | 📅 2026-08-28 - High-quality PDF-to-Markdown and JSON extraction, including formulas and tables, for building private corpora.
* [Docling](https://github.com/docling-project/docling) ⭐ 65,667 | 🐛 977 | 🌐 Python | 📅 2026-08-26 - Parse PDF, DOCX, PPTX, and HTML into structured formats for RAG and training, running entirely on your own hardware.
* [Marker](https://github.com/datalab-to/marker) ⭐ 39,336 | 🐛 457 | 🌐 Python | 📅 2026-08-27 - Fast, accurate document-to-Markdown conversion across PDFs, images, and office formats.
* [Label Studio](https://github.com/HumanSignal/label-studio) ⭐ 28,161 | 🐛 927 | 🌐 TypeScript | 📅 2026-08-28 - Self-hosted data labelling platform for text, image, audio, and video annotation.
* [Unstructured](https://github.com/Unstructured-IO/unstructured) ⭐ 15,354 | 🐛 296 | 🌐 HTML | 📅 2026-08-28 - Ingestion and preprocessing library for turning messy documents into model-ready chunks.
* [Argilla](https://github.com/argilla-io/argilla) ⭐ 5,088 | 🐛 29 | 🌐 Python | 📅 2026-08-24 - Collaborative tool for curating, annotating, and quality-checking datasets for fine-tuning and evaluation.
* [OpenWebText](https://skylion007.github.io/OpenWebTextCorpus/) - Open dataset similar to GPT training data.
* [RedPajama](https://www.together.xyz/blog/redpajama) - Open LLM training dataset.

## Learning Resources & Research

> Guides, papers, and tutorials on private AI.

* [LLMs from Scratch](https://github.com/rasbt/LLMs-from-scratch) ⭐ 103,922 | 🐛 2 | 🌐 Jupyter Notebook | 📅 2026-08-26 - Build a GPT-style model step by step in PyTorch, on your own machine.
* [LLM Course](https://github.com/mlabonne/llm-course) ⭐ 82,040 | 🐛 89 | 📅 2026-02-05 - Roadmap and notebooks covering LLM fundamentals, fine-tuning, quantization, and deployment.
* [ML Engineering Open Book](https://github.com/stas00/ml-engineering) ⭐ 18,799 | 🐛 4 | 🌐 Python | 📅 2026-08-27 - Field-tested notes on training and serving large models: hardware, parallelism, throughput, and debugging.
* [Smol Course](https://github.com/huggingface/smol-course) ⭐ 6,730 | 🐛 97 | 🌐 Jupyter Notebook | 📅 2026-08-20 - Hugging Face's practical course on aligning and fine-tuning small models that fit on local hardware.

## AI Routers & API Aggregators

> Centralized routers and proxy layers for aggregating, governing, and securing your private AI stack. These tools simplify connections to multiple model servers, optimize LLM routing, and provide observability, security, and compliance.

* [LiteLLM](https://github.com/BerriAI/litellm) ⭐ 57,438 | 🐛 4,856 | 🌐 Python | 📅 2026-08-28 - Self-hosted proxy exposing 100+ model backends — including Ollama, vLLM, and any OpenAI-compatible server — behind one API, with keys, budgets, routing, and logging.
* [Nexus](https://github.com/grafbase/nexus) ⭐ 435 | 🐛 28 | 🌐 Rust | 📅 2026-03-16 - Open-source AI router to aggregate Model Context Protocol (MCP) servers, intelligently route requests to the best LLMs, and provide security, governance, observability, and simplified architecture for private AI deployments. [Blog](https://nexusrouter.com/blog/introducing-nexus-the-open-source-ai-router)

## Contributing

Contributions welcome! See [Contributing](CONTRIBUTING.md)

## License

Under CC0-1.0 license. see [LICENSE](LICENSE)

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-28._
