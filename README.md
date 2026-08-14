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

* [llama.cpp](https://github.com/ggml-org/llama.cpp) ⭐ 123,929 | 🐛 2,035 | 🌐 C++ | 📅 2026-08-14 - Portable, CPU/GPU-friendly LLM inference, good for GPU + CPU hybrid inference.
* [vLLM](https://github.com/vllm-project/vllm) ⭐ 89,061 | 🐛 6,600 | 🌐 Python | 📅 2026-08-14 - High-throughput, low-latency inference engine for LLMs.
* [Cherry Studio](https://github.com/CherryHQ/cherry-studio) ⭐ 50,477 | 🐛 1,296 | 🌐 TypeScript | 📅 2026-08-14 - Powerful and customizable cross-platform desktop app for LLM inference with built in web search, RAG, MCP support, and a quick assistant hotkey to summon your LLM from anywhere. Supports a wide variety of providers and OpenAI compatible endpoints for local inference.
* [LocalAI](https://github.com/mudler/LocalAI) ⭐ 48,463 | 🐛 161 | 🌐 Go | 📅 2026-08-14 - Drop-in OpenAI-compatible API for local inference across text, image, audio, and embedding models, with no GPU required.
* [exo](https://github.com/exo-explore/exo) ⭐ 46,828 | 🐛 334 | 🌐 Python | 📅 2026-06-23 - Run your own AI cluster at home with everyday devices. Dynamic model partitioning across multiple devices like iPhones, Macs, and Linux machines.
* [sglang](https://github.com/sgl-project/sglang) ⭐ 31,808 | 🐛 4,913 | 🌐 Python | 📅 2026-08-14 - Fast serving engine for LLMs and vision-language models, with RadixAttention prefix caching and a structured generation language.
* [llamafile](https://github.com/Mozilla-Ocho/llamafile) ⭐ 25,567 | 🐛 212 | 🌐 C++ | 📅 2026-08-03 - Distribute and run an entire LLM as a single executable file that works across six operating systems, with no install step.
* [MLC LLM](https://github.com/mlc-ai/mlc-llm) ⭐ 23,060 | 🐛 334 | 🌐 Python | 📅 2026-07-31 - Compiler and runtime that deploys LLMs natively to GPUs, phones, and browsers via machine learning compilation.
* [KTransformers](https://github.com/kvcache-ai/ktransformers) ⭐ 19,235 | 🐛 502 | 🌐 Python | 📅 2026-08-08 - Optimized framework for running very large MoE models on limited hardware via GPU/CPU offloading and kernel injection.
* [oMLX](https://github.com/jundot/omlx) ⭐ 18,695 | 🐛 862 | 🌐 Python | 📅 2026-08-14 - macOS-native MLX inference server with paged SSD KV caching and continuous batching. Serves LLM, VLM, embedding, and reranker models over OpenAI- and Anthropic-compatible endpoints for local coding agents on Apple Silicon.
* [text-generation-inference](https://github.com/huggingface/text-generation-inference) ⚠️ Archived - Optimized serving stack from Hugging Face.
* [mlx-lm](https://github.com/ml-explore/mlx-lm) ⭐ 6,612 | 🐛 635 | 🌐 Python | 📅 2026-08-12 - Fast, Apple Silicon-optimized LLM inference engine for running models locally and privately.
* [llama-swap](https://github.com/mostlygeek/llama-swap) ⭐ 5,352 | 🐛 76 | 🌐 Go | 📅 2026-08-14 - Model swapping for llama.cpp (or any local OpenAPI compatible server).
* [ik\_llama.cpp](https://github.com/ikawrakow/ik_llama.cpp) ⭐ 3,033 | 🐛 83 | 🌐 C++ | 📅 2026-08-14 - Fork of llama.cpp with bleeding edge feature implementations and quantization improvements.
* [RamaLama](https://github.com/containers/ramalama) ⭐ 3,000 | 🐛 108 | 🌐 Python | 📅 2026-08-10 - Runs models as OCI containers, pulling from registries you control — a good fit for air-gapped and enterprise workflows.
* [tabbyAPI](https://github.com/theroyallab/tabbyAPI) ⭐ 1,302 | 🐛 32 | 🌐 Python | 📅 2026-08-13 - Official API server for running exllamav2 and exllamav3 models. Aims to be a friendly backend with high customizablity and an idiotmatic OAI compatible API for users.
* [exllama3](https://github.com/turboderp-org/exllamav3) ⭐ 1,132 | 🐛 53 | 🌐 Python | 📅 2026-08-12 - An optimized quantization and inference library for running LLMs locally on modern consumer-class GPUs. Use TabbyAPI for an API server.
* [YALS (Yet another llamacpp server)](https://github.com/theroyallab/YALS) ⭐ 99 | 🐛 4 | 🌐 TypeScript | 📅 2026-03-28 - TabbyAPI's sister project, adapted for llama.cpp and GGUF models. Built from the ground up using libllama instead of wrapping llama-server.
* [Jan](https://jan.ai/) - Privacy-first, offline AI assistant and LLM runtime for local, secure inference.
* [LM Studio](https://lmstudio.ai/) - Cross-platform desktop app for running local LLMs with an easy-to-use interface.
* [LLM-D](https://llm-d.ai/) - Privacy-first, distributed LLM inference engine for scalable, local deployments.
* [Ollama](https://ollama.com) - Local LLM runner with model packaging. Uses llama.cpp backend to serve cautious model defaults.
* [GPT4All](https://gpt4all.io) - Local desktop model runner.

## Model Management & Serving

> Tools for hosting, scaling, and versioning AI models privately.

* [Triton Inference Server](https://github.com/triton-inference-server/server) ⭐ 10,920 | 🐛 907 | 🌐 Python | 📅 2026-08-14 - NVIDIA's multi-framework inference server, supporting TensorRT, PyTorch, ONNX, and vLLM backends behind one endpoint.
* [Xinference](https://github.com/xorbitsai/inference) ⭐ 9,495 | 🐛 43 | 🌐 Python | 📅 2026-08-14 - Serve and manage LLM, embedding, rerank, image, and audio models in one self-hosted cluster with an OpenAI-compatible API.
* [Seldon Core](https://github.com/SeldonIO/seldon-core) ⭐ 4,770 | 🐛 396 | 🌐 Go | 📅 2026-03-23 - Kubernetes-native model deployment.
* [vLLM Production Stack](https://github.com/vllm-project/production-stack) ⭐ 2,508 | 🐛 179 | 🌐 Python | 📅 2026-08-13 - End-to-end stack for deploying vLLM in production, including orchestration, monitoring, autoscaling, and best practices for private LLM serving.
* [OME (Open Model Engine)](https://github.com/sgl-project/ome) ⭐ 492 | 🐛 122 | 🌐 Go | 📅 2026-08-14 - Unified, open-source engine for serving, managing, and scaling LLMs and multimodal models privately. Supports sglang, vLLM, and more.
* [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - Scalable Python model serving.
* [KServe](https://kserve.github.io/website/) - Serverless model inference on Kubernetes.
* [BentoML](https://www.bentoml.com/) - Model packaging & serving framework.

## Fine-Tuning & Adapters

> Private workflows for adapting models to your needs.

* [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) ⭐ 74,097 | 🐛 1,113 | 🌐 Python | 📅 2026-08-13 - Unified fine-tuning for 100+ models with a web UI, covering SFT, DPO, PPO, and reward modelling on your own hardware.
* [Unsloth](https://github.com/unslothai/unsloth) ⭐ 71,446 | 🐛 1,160 | 🌐 Python | 📅 2026-08-14 - Fine-tune and reinforcement-train LLMs 2x faster with substantially less VRAM, on a single local GPU.
* [PEFT](https://github.com/huggingface/peft) ⭐ 21,545 | 🐛 63 | 🌐 Python | 📅 2026-08-14 - Parameter-efficient fine-tuning.
* [TRL](https://github.com/huggingface/trl) ⭐ 19,071 | 🐛 281 | 🌐 Python | 📅 2026-08-14 - Hugging Face's library for SFT, DPO, GRPO, and reward-model training on top of transformers.
* [ms-swift](https://github.com/modelscope/ms-swift) ⭐ 15,170 | 🐛 655 | 🌐 Python | 📅 2026-08-14 - Training and deployment toolkit covering 500+ LLMs and 200+ multimodal models, from PEFT through to quantized export.
* [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) ⭐ 12,357 | 🐛 268 | 🌐 Python | 📅 2026-08-13 - YAML-driven post-training framework covering full fine-tunes, LoRA, QLoRA, and multi-GPU sharding.
* [torchtune](https://github.com/pytorch/torchtune) ⭐ 5,797 | 🐛 455 | 🌐 Python | 📅 2026-08-14 - Native PyTorch library for fine-tuning and experimenting with LLMs, with readable single-file recipes.
* [LoRA](https://arxiv.org/abs/2106.09685) - Low-rank adaptation technique.
* [QLoRA](https://arxiv.org/abs/2305.14314) - Memory-efficient LoRA on quantized models.

## Quantization & Compression

> Shrink models to fit the hardware you actually own.

* [bitsandbytes](https://github.com/bitsandbytes-foundation/bitsandbytes) ⭐ 8,414 | 🐛 56 | 🌐 Python | 📅 2026-08-13 - 8-bit and 4-bit quantization primitives that underpin QLoRA and much of the local fine-tuning ecosystem.
* [llm-compressor](https://github.com/vllm-project/llm-compressor) ⭐ 3,678 | 🐛 143 | 🌐 Python | 📅 2026-08-14 - Apply GPTQ, SmoothQuant, SparseGPT, and FP8/INT4 weight-activation quantization, exporting straight to vLLM.
* [GPTQModel](https://github.com/ModelCloud/GPTQModel) ⭐ 1,228 | 🐛 42 | 🌐 Python | 📅 2026-08-13 - Actively maintained GPTQ toolkit for producing and running 4-bit quantized models.

## Vector Databases & Embeddings

> Private semantic search & retrieval-augmented generation.

* [FAISS](https://github.com/facebookresearch/faiss) ⭐ 40,741 | 🐛 277 | 🌐 C++ | 📅 2026-08-13 - Facebook AI Similarity Search.
* [Qdrant](https://github.com/qdrant/qdrant) ⭐ 33,975 | 🐛 689 | 🌐 Rust | 📅 2026-08-14 - High-performance Vector Database and Vector Search Engine.
* [pgvector](https://github.com/pgvector/pgvector) ⭐ 22,628 | 🐛 14 | 🌐 C | 📅 2026-08-14 - Vector similarity search inside PostgreSQL, keeping embeddings in the database you already self-host.
* [LanceDB](https://github.com/lancedb/lancedb) ⭐ 11,148 | 🐛 619 | 🌐 Rust | 📅 2026-08-14 - Embedded, serverless vector database that stores vectors and metadata as files on your own disk or object store.
* [text-embeddings-inference](https://github.com/huggingface/text-embeddings-inference) ⭐ 5,000 | 🐛 207 | 🌐 Rust | 📅 2026-07-24 - Fast local serving for embedding and reranker models, so retrieval never leaves your network.
* [Milvus](https://milvus.io) - Scalable vector database.
* [Weaviate](https://weaviate.io) - Open-source semantic search engine.
* [Chroma](https://www.trychroma.com/) - Local-first vector database.

## Agents & Orchestration

> Frameworks for chaining private AI tools & agents.

* [Langflow](https://github.com/langflow-ai/langflow) ⭐ 153,247 | 🐛 972 | 🌐 Python | 📅 2026-08-14 - Visual workflow builder for creating and deploying AI-powered agents and workflows with built-in API servers.
* [MetaGPT](https://github.com/FoundationAgents/MetaGPT) ⭐ 69,814 | 🐛 129 | 🌐 Python | 📅 2026-01-21 - Multi-agent framework for building collaborative AI systems with role-based agents that can work together on complex tasks.
* [Flowise](https://github.com/FlowiseAI/Flowise) ⚠️ Archived - No-code LangChain UI.
* [Goose](https://github.com/block/goose) ⭐ 52,808 | 🐛 271 | 🌐 Rust | 📅 2026-08-14 - Local, extensible agent that runs on your machine and works against any LLM backend, including Ollama and other self-hosted endpoints.
* [Aider](https://github.com/Aider-AI/aider) ⭐ 48,205 | 🐛 1,798 | 🌐 Python | 📅 2026-05-22 - Terminal-based pair programming agent that edits code in your local git repo, with support for local models via Ollama and OpenAI-compatible servers.
* [dspy](https://github.com/stanfordnlp/dspy) ⭐ 37,189 | 🐛 653 | 🌐 Python | 📅 2026-08-14 - Modular, open-source agent framework for building composable, private LLM applications and workflows.
* [Crush](https://github.com/charmbracelet/crush) ⭐ 27,382 | 🐛 629 | 🌐 Go | 📅 2026-08-14 - Privacy-first, open-source agentic coding and automation platform for local AI workflows.
* [CUA](https://github.com/trycua/cua) ⭐ 21,351 | 🐛 643 | 🌐 HTML | 📅 2026-08-14 -  enables AI agents to control full operating systems in virtual containers and deploy them locally or to the cloud.
* [PydanticAI](https://github.com/pydantic/pydantic-ai) ⭐ 19,296 | 🐛 691 | 🌐 Python | 📅 2026-08-14 - Python agent framework by the Pydantic team, model-agnostic with Ollama support for local deployment.
* [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) ⭐ 16,968 | 🐛 520 | 🌐 Python | 📅 2026-03-04 - Open-source, privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
* [DeepCode](https://github.com/HKUDS/DeepCode) ⭐ 16,356 | 🐛 26 | 🌐 Python | 📅 2026-08-14 - Open agentic coding framework that turns papers and specs into working code (Paper2Code, Text2Web, Text2Backend), running against local Ollama or vLLM backends.
* [Trae Agent](https://github.com/bytedance/trae-agent) ⭐ 12,021 | 🐛 159 | 🌐 Python | 📅 2026-02-05 - Privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
* [Bytebot](https://github.com/bytebot-ai/bytebot) ⚠️ Archived - A desktop agent is an AI that has its own computer. Unlike browser-only agents or traditional RPA tools, Bytebot comes with a full virtual desktop.
* [AG2](https://github.com/ag2ai/ag2) ⭐ 4,859 | 🐛 21 | 🌐 Python | 📅 2026-08-14 - Open-source operating system for agentic AI with native Ollama support for local model deployment and multi-agent collaboration.
* [agentgateway](https://github.com/agentgateway/agentgateway) ⭐ 4,357 | 🐛 332 | 🌐 Rust | 📅 2026-08-14 - Gateway for managing and orchestrating AI agents with support for local deployment.
* [Skales](https://github.com/skalesapp/skales) ⭐ 1,637 | 🐛 4 | 🌐 TypeScript | 📅 2026-08-13 - Source-available (BSL 1.1) local-first desktop AI agent that runs fully on-device, offline via Ollama or with 15+ providers; your files never leave your machine, no cloud required.
* [MFS](https://github.com/zilliztech/mfs) ⭐ 119 | 🐛 2 | 🌐 Python | 📅 2026-07-31 - Exposes your code, docs, chat (Slack/Gmail/Jira), databases and object stores as one file-like, searchable namespace for agents (`ls`/`cat`/`grep` + semantic search); runs fully local with on-device ONNX embeddings on Milvus, no API key.
* [LangChain](https://www.langchain.com/) - Agent and LLM orchestration framework.
* [Haystack](https://haystack.deepset.ai) - End-to-end RAG pipelines.
* [LlamaIndex](https://www.llamaindex.ai) - Data framework for LLM apps.
* [Herdr](https://herdr.dev/) - Self-hosted runtime and terminal multiplexer for coding agents. Runs the agent CLIs on your own machine or a box you control, grouping them into workspaces you can detach from and reattach to over SSH.
* [OpenCode AI](https://opencode.ai/) - Open-source agentic coding platform for private, local, and secure AI-powered development workflows.

## VS Code Plugins & Extensions

> Privacy-first, open-source agentic coding plugins and extensions for VS Code and other editors.

* [cline](https://github.com/cline/cline) ⭐ 66,192 | 🐛 995 | 🌐 TypeScript | 📅 2026-08-14 - Privacy-first, open-source agentic coding platform for local AI workflows and automation (VS Code extension).
* [Continue](https://github.com/continuedev/continue) ⭐ 35,478 | 🐛 942 | 🌐 TypeScript | 📅 2026-08-14 - Open-source autocomplete and chat assistant for VS Code and JetBrains, configurable against Ollama, llama.cpp, vLLM, and other local endpoints.
* [Tabby](https://github.com/TabbyML/tabby) ⭐ 33,823 | 🐛 330 | 🌐 Rust | 📅 2026-06-30 - Self-hosted AI coding assistant with its own inference server, offering a private alternative to hosted completion services.
* [Roo Code](https://github.com/RooCodeInc/Roo-Code) ⚠️ Archived - Privacy-first, open-source agentic coding platform for secure, local AI development (VS Code extension).

## Privacy, Security & Governance

> Keep AI deployments secure and compliant.

* [Presidio](https://github.com/microsoft/presidio) ⭐ 10,485 | 🐛 105 | 🌐 Python | 📅 2026-08-11 - Detect and de-identify PII in text and images before it ever reaches a model.
* [garak](https://github.com/NVIDIA/garak) ⭐ 8,800 | 🐛 391 | 🌐 Python | 📅 2026-08-13 - LLM vulnerability scanner that probes local models for prompt injection, jailbreaks, and data leakage.
* [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) ⭐ 6,951 | 🐛 216 | 🌐 Python | 📅 2026-08-13 - Add programmable topical and safety rails to LLM applications, running alongside self-hosted models.
* [LLM Guard](https://github.com/protectai/llm-guard) ⚠️ Archived - Input and output scanning toolkit covering prompt injection, PII, toxicity, and secrets leakage.
* [Concrete](https://github.com/zama-ai/concrete) ⭐ 1,572 | 🐛 56 | 🌐 C++ | 📅 2025-12-19 - Fully homomorphic encryption for AI.
* [OpenFL](https://github.com/securefederatedai/openfl) ⭐ 842 | 🐛 83 | 🌐 Python | 📅 2026-02-21 - Federated learning framework.
* [BlindAI](https://github.com/mithril-security/blindai) ⭐ 511 | 🐛 6 | 🌐 Rust | 📅 2024-03-19 - Confidential AI inference using TEEs.
* [Flower](https://flower.dev) - Federated learning at scale.

## Observability & Evaluation

> Measure and monitor private deployments without shipping traces to a vendor.

* [Langfuse](https://github.com/langfuse/langfuse) ⭐ 33,113 | 🐛 779 | 🌐 TypeScript | 📅 2026-08-14 - Self-hostable LLM observability, tracing, prompt management, and evaluation.
* [promptfoo](https://github.com/promptfoo/promptfoo) ⭐ 24,237 | 🐛 497 | 🌐 TypeScript | 📅 2026-08-14 - Local-first evaluation and red-teaming for prompts and models, runnable entirely offline in CI.
* [DeepEval](https://github.com/confident-ai/deepeval) ⭐ 17,597 | 🐛 464 | 🌐 Python | 📅 2026-08-13 - Unit-testing framework for LLM outputs, with metrics that can run against locally hosted judge models.
* [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) ⭐ 13,635 | 🐛 927 | 🌐 Python | 📅 2026-08-14 - The standard harness for benchmarking language models, supporting local vLLM and Hugging Face backends.
* [Phoenix](https://github.com/Arize-ai/phoenix) ⭐ 11,053 | 🐛 921 | 🌐 Python | 📅 2026-08-14 - Self-hosted tracing, evaluation, and experiment tracking for LLM applications.

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

* [Open WebUI](https://github.com/open-webui/open-webui) ⭐ 148,799 | 🐛 393 | 🌐 Python | 📅 2026-08-14 - Commonly recommended Web UI frontend which features built in search, web scrape, RAG, and optional user authentication.
* [Lobe Chat](https://github.com/lobehub/lobe-chat) ⭐ 81,693 | 🐛 739 | 🌐 TypeScript | 📅 2026-08-14 - Modern self-hosted chat framework with plugin and multimodal support, deployable in one click against local backends.
* [text-generation-webui](https://github.com/oobabooga/text-generation-webui) ⭐ 47,545 | 🐛 832 | 🌐 Python | 📅 2026-06-02 - Long-standing Gradio web UI for local text generation, supporting llama.cpp, ExLlama, and transformers backends.
* [LibreChat](https://github.com/danny-avila/LibreChat) ⭐ 42,030 | 🐛 707 | 🌐 TypeScript | 📅 2026-08-14 - Enhanced web UI for LLMs.
* [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) ⭐ 33,336 | 🐛 241 | 🌐 TypeScript | 📅 2024-08-03 - Open-source ChatGPT clone.
* [SillyTavern](https://github.com/SillyTavern/SillyTavern) ⭐ 32,117 | 🐛 581 | 🌐 JavaScript | 📅 2026-07-11 - Self-hosted, highly customizable frontend for local models, with extensive character, prompt, and context management.
* [Screenpipe](https://github.com/screenpipe/screenpipe) ⭐ 20,958 | 🐛 100 | 🌐 Rust | 📅 2026-08-14 - 24/7 local screen + microphone recording with OCR, audio transcription, and semantic search. Fully offline with Ollama or any local LLM. MCP server for Claude.
* [AnythingLLM](https://anythingllm.com/) - Full-stack private LLM workspace.

## Image & Video Generation

> Run diffusion and video models on your own GPUs.

* [AUTOMATIC1111 Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) ⭐ 164,515 | 🐛 2,502 | 🌐 Python | 📅 2026-03-02 - The most widely deployed self-hosted Stable Diffusion interface, with a large extension ecosystem.
* [ComfyUI](https://github.com/comfyanonymous/ComfyUI) ⭐ 127,577 | 🐛 4,582 | 🌐 Python | 📅 2026-08-14 - Node-based interface and backend for diffusion models, running image, video, and audio pipelines entirely locally.
* [InvokeAI](https://github.com/invoke-ai/InvokeAI) ⭐ 27,891 | 🐛 393 | 🌐 Python | 📅 2026-08-13 - Professional-grade local generative image toolkit with a unified canvas and workflow editor.

## Speech & Audio

> Private speech-to-text and text-to-speech.

* [Whisper](https://github.com/openai/whisper) ⭐ 107,269 | 🐛 135 | 🌐 Python | 📅 2026-07-28 - The original open-weight speech recognition model, runnable fully offline.
* [whisper.cpp](https://github.com/ggml-org/whisper.cpp) ⭐ 52,891 | 🐛 1,242 | 🌐 C++ | 📅 2026-08-14 - C++ port of OpenAI's Whisper automatic speech recognition model, optimized for local, CPU/GPU inference without internet connectivity.
* [WhisperX](https://github.com/m-bain/whisperX) ⭐ 23,572 | 🐛 211 | 🌐 Python | 📅 2026-07-13 - Whisper with word-level timestamps, speaker diarization, and much faster batched transcription.
* [F5-TTS](https://github.com/SWivid/F5-TTS) ⭐ 15,118 | 🐛 58 | 🌐 Python | 📅 2026-07-23 - Local text-to-speech with voice cloning from a short reference sample.
* [RealtimeSTT](https://github.com/KoljaB/RealtimeSTT) ⭐ 10,054 | 🐛 147 | 🌐 Python | 📅 2026-06-12 - Low-latency local speech-to-text with voice activity detection, for building private voice interfaces.
* [speaches](https://github.com/speaches-ai/speaches) ⭐ 3,587 | 🐛 141 | 🌐 Python | 📅 2026-08-13 - Self-hosted OpenAI-compatible server for transcription, translation, and speech generation.

## Datasets & Data Prep

> Create and manage private training corpora.

* [MinerU](https://github.com/opendatalab/MinerU) ⭐ 77,637 | 🐛 101 | 🌐 Python | 📅 2026-08-14 - High-quality PDF-to-Markdown and JSON extraction, including formulas and tables, for building private corpora.
* [Docling](https://github.com/docling-project/docling) ⭐ 64,773 | 🐛 961 | 🌐 Python | 📅 2026-08-14 - Parse PDF, DOCX, PPTX, and HTML into structured formats for RAG and training, running entirely on your own hardware.
* [Marker](https://github.com/datalab-to/marker) ⭐ 38,743 | 🐛 450 | 🌐 Python | 📅 2026-08-07 - Fast, accurate document-to-Markdown conversion across PDFs, images, and office formats.
* [Label Studio](https://github.com/HumanSignal/label-studio) ⭐ 28,058 | 🐛 923 | 🌐 TypeScript | 📅 2026-08-14 - Self-hosted data labelling platform for text, image, audio, and video annotation.
* [Unstructured](https://github.com/Unstructured-IO/unstructured) ⭐ 15,311 | 🐛 287 | 🌐 HTML | 📅 2026-08-14 - Ingestion and preprocessing library for turning messy documents into model-ready chunks.
* [Argilla](https://github.com/argilla-io/argilla) ⭐ 5,080 | 🐛 29 | 🌐 Python | 📅 2026-08-10 - Collaborative tool for curating, annotating, and quality-checking datasets for fine-tuning and evaluation.
* [OpenWebText](https://skylion007.github.io/OpenWebTextCorpus/) - Open dataset similar to GPT training data.
* [RedPajama](https://www.together.xyz/blog/redpajama) - Open LLM training dataset.

## Learning Resources & Research

> Guides, papers, and tutorials on private AI.

* [LLMs from Scratch](https://github.com/rasbt/LLMs-from-scratch) ⭐ 102,664 | 🐛 2 | 🌐 Jupyter Notebook | 📅 2026-08-10 - Build a GPT-style model step by step in PyTorch, on your own machine.
* [LLM Course](https://github.com/mlabonne/llm-course) ⭐ 81,671 | 🐛 87 | 📅 2026-02-05 - Roadmap and notebooks covering LLM fundamentals, fine-tuning, quantization, and deployment.
* [ML Engineering Open Book](https://github.com/stas00/ml-engineering) ⭐ 18,616 | 🐛 3 | 🌐 Python | 📅 2026-08-14 - Field-tested notes on training and serving large models: hardware, parallelism, throughput, and debugging.
* [Smol Course](https://github.com/huggingface/smol-course) ⭐ 6,725 | 🐛 96 | 🌐 Jupyter Notebook | 📅 2026-05-26 - Hugging Face's practical course on aligning and fine-tuning small models that fit on local hardware.

## AI Routers & API Aggregators

> Centralized routers and proxy layers for aggregating, governing, and securing your private AI stack. These tools simplify connections to multiple model servers, optimize LLM routing, and provide observability, security, and compliance.

* [LiteLLM](https://github.com/BerriAI/litellm) ⭐ 56,352 | 🐛 4,942 | 🌐 Python | 📅 2026-08-14 - Self-hosted proxy exposing 100+ model backends — including Ollama, vLLM, and any OpenAI-compatible server — behind one API, with keys, budgets, routing, and logging.
* [Nexus](https://github.com/grafbase/nexus) ⭐ 434 | 🐛 28 | 🌐 Rust | 📅 2026-03-16 - Open-source AI router to aggregate Model Context Protocol (MCP) servers, intelligently route requests to the best LLMs, and provide security, governance, observability, and simplified architecture for private AI deployments. [Blog](https://nexusrouter.com/blog/introducing-nexus-the-open-source-ai-router)

## Contributing

Contributions welcome! See [Contributing](CONTRIBUTING.md)

## License

Under CC0-1.0 license. see [LICENSE](LICENSE)

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-14._
