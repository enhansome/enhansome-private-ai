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

* [llama.cpp](https://github.com/ggml-org/llama.cpp) ⭐ 128,591 | 🐛 2,492 | 🌐 C++ | 📅 2026-09-17 - Portable, CPU/GPU-friendly LLM inference, good for GPU + CPU hybrid inference.
* [vLLM](https://github.com/vllm-project/vllm) ⭐ 92,030 | 🐛 8,075 | 🌐 Python | 📅 2026-09-17 - High-throughput, low-latency inference engine for LLMs.
* [Cherry Studio](https://github.com/CherryHQ/cherry-studio) ⭐ 51,924 | 🐛 1,547 | 🌐 TypeScript | 📅 2026-09-17 - Powerful and customizable cross-platform desktop app for LLM inference with built in web search, RAG, MCP support, and a quick assistant hotkey to summon your LLM from anywhere. Supports a wide variety of providers and OpenAI compatible endpoints for local inference.
* [LocalAI](https://github.com/mudler/LocalAI) ⭐ 49,145 | 🐛 188 | 🌐 Go | 📅 2026-09-17 - Drop-in OpenAI-compatible API for local inference across text, image, audio, and embedding models, with no GPU required.
* [exo](https://github.com/exo-explore/exo) ⭐ 47,485 | 🐛 373 | 🌐 Python | 📅 2026-08-25 - Run your own AI cluster at home with everyday devices. Dynamic model partitioning across multiple devices like iPhones, Macs, and Linux machines.
* [sglang](https://github.com/sgl-project/sglang) ⭐ 36,109 | 🐛 5,432 | 🌐 Python | 📅 2026-09-17 - Fast serving engine for LLMs and vision-language models, with RadixAttention prefix caching and a structured generation language.
* [llamafile](https://github.com/Mozilla-Ocho/llamafile) ⭐ 25,985 | 🐛 211 | 🌐 C++ | 📅 2026-09-16 - Distribute and run an entire LLM as a single executable file that works across six operating systems, with no install step.
* [MLC LLM](https://github.com/mlc-ai/mlc-llm) ⭐ 23,165 | 🐛 343 | 🌐 Python | 📅 2026-08-17 - Compiler and runtime that deploys LLMs natively to GPUs, phones, and browsers via machine learning compilation.
* [oMLX](https://github.com/jundot/omlx) ⭐ 21,846 | 🐛 1,371 | 🌐 Python | 📅 2026-09-17 - macOS-native MLX inference server with paged SSD KV caching and continuous batching. Serves LLM, VLM, embedding, and reranker models over OpenAI- and Anthropic-compatible endpoints for local coding agents on Apple Silicon.
* [KTransformers](https://github.com/kvcache-ai/ktransformers) ⭐ 19,523 | 🐛 510 | 🌐 Python | 📅 2026-09-17 - Optimized framework for running very large MoE models on limited hardware via GPU/CPU offloading and kernel injection.
* [text-generation-inference](https://github.com/huggingface/text-generation-inference) ⚠️ Archived - Optimized serving stack from Hugging Face.
* [mlx-lm](https://github.com/ml-explore/mlx-lm) ⭐ 7,043 | 🐛 217 | 🌐 Python | 📅 2026-09-17 - Fast, Apple Silicon-optimized LLM inference engine for running models locally and privately.
* [llama-swap](https://github.com/mostlygeek/llama-swap) ⭐ 5,688 | 🐛 82 | 🌐 Go | 📅 2026-09-17 - Model swapping for llama.cpp (or any local OpenAPI compatible server).
* [ik\_llama.cpp](https://github.com/ikawrakow/ik_llama.cpp) ⭐ 3,236 | 🐛 106 | 🌐 C++ | 📅 2026-09-17 - Fork of llama.cpp with bleeding edge feature implementations and quantization improvements.
* [RamaLama](https://github.com/containers/ramalama) ⭐ 3,050 | 🐛 115 | 🌐 Python | 📅 2026-09-17 - Runs models as OCI containers, pulling from registries you control — a good fit for air-gapped and enterprise workflows.
* [exllama3](https://github.com/turboderp-org/exllamav3) ⭐ 1,433 | 🐛 66 | 🌐 Python | 📅 2026-09-17 - An optimized quantization and inference library for running LLMs locally on modern consumer-class GPUs. Use TabbyAPI for an API server.
* [tabbyAPI](https://github.com/theroyallab/tabbyAPI) ⭐ 1,394 | 🐛 39 | 🌐 Python | 📅 2026-09-13 - Official API server for running exllamav2 and exllamav3 models. Aims to be a friendly backend with high customizablity and an idiotmatic OAI compatible API for users.
* [YALS (Yet another llamacpp server)](https://github.com/theroyallab/YALS) ⭐ 101 | 🐛 4 | 🌐 TypeScript | 📅 2026-03-28 - TabbyAPI's sister project, adapted for llama.cpp and GGUF models. Built from the ground up using libllama instead of wrapping llama-server.
* [Jan](https://jan.ai/) - Privacy-first, offline AI assistant and LLM runtime for local, secure inference.
* [LM Studio](https://lmstudio.ai/) - Cross-platform desktop app for running local LLMs with an easy-to-use interface.
* [LLM-D](https://llm-d.ai/) - Privacy-first, distributed LLM inference engine for scalable, local deployments.
* [Ollama](https://ollama.com) - Local LLM runner with model packaging. Uses llama.cpp backend to serve cautious model defaults.
* [GPT4All](https://gpt4all.io) - Local desktop model runner.

## Model Management & Serving

> Tools for hosting, scaling, and versioning AI models privately.

* [Triton Inference Server](https://github.com/triton-inference-server/server) ⭐ 10,994 | 🐛 894 | 🌐 Python | 📅 2026-09-17 - NVIDIA's multi-framework inference server, supporting TensorRT, PyTorch, ONNX, and vLLM backends behind one endpoint.
* [Xinference](https://github.com/xorbitsai/inference) ⭐ 9,575 | 🐛 40 | 🌐 Python | 📅 2026-09-17 - Serve and manage LLM, embedding, rerank, image, and audio models in one self-hosted cluster with an OpenAI-compatible API.
* [Seldon Core](https://github.com/SeldonIO/seldon-core) ⭐ 4,781 | 🐛 396 | 🌐 Go | 📅 2026-03-23 - Kubernetes-native model deployment.
* [vLLM Production Stack](https://github.com/vllm-project/production-stack) ⭐ 2,591 | 🐛 218 | 🌐 Python | 📅 2026-09-14 - End-to-end stack for deploying vLLM in production, including orchestration, monitoring, autoscaling, and best practices for private LLM serving.
* [OME (Open Model Engine)](https://github.com/sgl-project/ome) ⭐ 509 | 🐛 142 | 🌐 Go | 📅 2026-09-17 - Unified, open-source engine for serving, managing, and scaling LLMs and multimodal models privately. Supports sglang, vLLM, and more.
* [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) - Scalable Python model serving.
* [KServe](https://kserve.github.io/website/) - Serverless model inference on Kubernetes.
* [BentoML](https://www.bentoml.com/) - Model packaging & serving framework.

## Fine-Tuning & Adapters

> Private workflows for adapting models to your needs.

* [Unsloth](https://github.com/unslothai/unsloth) ⭐ 76,312 | 🐛 1,235 | 🌐 Python | 📅 2026-09-17 - Fine-tune and reinforcement-train LLMs 2x faster with substantially less VRAM, on a single local GPU.
* [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) ⭐ 74,837 | 🐛 1,156 | 🌐 Python | 📅 2026-09-14 - Unified fine-tuning for 100+ models with a web UI, covering SFT, DPO, PPO, and reward modelling on your own hardware.
* [PEFT](https://github.com/huggingface/peft) ⭐ 21,691 | 🐛 81 | 🌐 Python | 📅 2026-09-17 - Parameter-efficient fine-tuning.
* [TRL](https://github.com/huggingface/trl) ⭐ 19,335 | 🐛 286 | 🌐 Python | 📅 2026-09-17 - Hugging Face's library for SFT, DPO, GRPO, and reward-model training on top of transformers.
* [ms-swift](https://github.com/modelscope/ms-swift) ⭐ 15,659 | 🐛 593 | 🌐 Python | 📅 2026-09-17 - Training and deployment toolkit covering 500+ LLMs and 200+ multimodal models, from PEFT through to quantized export.
* [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) ⭐ 12,484 | 🐛 244 | 🌐 Python | 📅 2026-09-17 - YAML-driven post-training framework covering full fine-tunes, LoRA, QLoRA, and multi-GPU sharding.
* [torchtune](https://github.com/pytorch/torchtune) ⭐ 5,812 | 🐛 467 | 🌐 Python | 📅 2026-09-09 - Native PyTorch library for fine-tuning and experimenting with LLMs, with readable single-file recipes.
* [LoRA](https://arxiv.org/abs/2106.09685) - Low-rank adaptation technique.
* [QLoRA](https://arxiv.org/abs/2305.14314) - Memory-efficient LoRA on quantized models.

## Quantization & Compression

> Shrink models to fit the hardware you actually own.

* [bitsandbytes](https://github.com/bitsandbytes-foundation/bitsandbytes) ⭐ 8,484 | 🐛 90 | 🌐 Python | 📅 2026-09-07 - 8-bit and 4-bit quantization primitives that underpin QLoRA and much of the local fine-tuning ecosystem.
* [llm-compressor](https://github.com/vllm-project/llm-compressor) ⭐ 3,791 | 🐛 109 | 🌐 Python | 📅 2026-09-17 - Apply GPTQ, SmoothQuant, SparseGPT, and FP8/INT4 weight-activation quantization, exporting straight to vLLM.
* [GPTQModel](https://github.com/ModelCloud/GPTQModel) ⭐ 1,257 | 🐛 41 | 🌐 Python | 📅 2026-09-17 - Actively maintained GPTQ toolkit for producing and running 4-bit quantized models.

## Vector Databases & Embeddings

> Private semantic search & retrieval-augmented generation.

* [FAISS](https://github.com/facebookresearch/faiss) ⭐ 40,926 | 🐛 326 | 🌐 C++ | 📅 2026-09-17 - Facebook AI Similarity Search.
* [Qdrant](https://github.com/qdrant/qdrant) ⭐ 34,640 | 🐛 731 | 🌐 Rust | 📅 2026-09-17 - High-performance Vector Database and Vector Search Engine.
* [pgvector](https://github.com/pgvector/pgvector) ⭐ 23,045 | 🐛 16 | 🌐 C | 📅 2026-09-10 - Vector similarity search inside PostgreSQL, keeping embeddings in the database you already self-host.
* [LanceDB](https://github.com/lancedb/lancedb) ⭐ 11,449 | 🐛 623 | 🌐 Rust | 📅 2026-09-17 - Embedded, serverless vector database that stores vectors and metadata as files on your own disk or object store.
* [text-embeddings-inference](https://github.com/huggingface/text-embeddings-inference) ⭐ 5,051 | 🐛 205 | 🌐 Rust | 📅 2026-09-17 - Fast local serving for embedding and reranker models, so retrieval never leaves your network.
* [Milvus](https://milvus.io) - Scalable vector database.
* [Weaviate](https://weaviate.io) - Open-source semantic search engine.
* [Chroma](https://www.trychroma.com/) - Local-first vector database.

## Agents & Orchestration

> Frameworks for chaining private AI tools & agents.

* [Langflow](https://github.com/langflow-ai/langflow) ⭐ 154,944 | 🐛 1,086 | 🌐 Python | 📅 2026-09-17 - Visual workflow builder for creating and deploying AI-powered agents and workflows with built-in API servers.
* [MetaGPT](https://github.com/FoundationAgents/MetaGPT) ⭐ 70,472 | 🐛 132 | 🌐 Python | 📅 2026-01-21 - Multi-agent framework for building collaborative AI systems with role-based agents that can work together on complex tasks.
* [Flowise](https://github.com/FlowiseAI/Flowise) ⚠️ Archived - No-code LangChain UI.
* [Goose](https://github.com/block/goose) ⭐ 54,391 | 🐛 361 | 🌐 Rust | 📅 2026-09-17 - Local, extensible agent that runs on your machine and works against any LLM backend, including Ollama and other self-hosted endpoints.
* [Aider](https://github.com/Aider-AI/aider) ⭐ 49,023 | 🐛 1,875 | 🌐 Python | 📅 2026-05-22 - Terminal-based pair programming agent that edits code in your local git repo, with support for local models via Ollama and OpenAI-compatible servers.
* [dspy](https://github.com/stanfordnlp/dspy) ⭐ 38,106 | 🐛 706 | 🌐 Python | 📅 2026-09-17 - Modular, open-source agent framework for building composable, private LLM applications and workflows.
* [Crush](https://github.com/charmbracelet/crush) ⭐ 28,150 | 🐛 756 | 🌐 Go | 📅 2026-09-17 - Privacy-first, open-source agentic coding and automation platform for local AI workflows.
* [CUA](https://github.com/trycua/cua) ⭐ 22,848 | 🐛 989 | 🌐 HTML | 📅 2026-09-17 -  enables AI agents to control full operating systems in virtual containers and deploy them locally or to the cloud.
* [PydanticAI](https://github.com/pydantic/pydantic-ai) ⭐ 20,014 | 🐛 916 | 🌐 Python | 📅 2026-09-17 - Python agent framework by the Pydantic team, model-agnostic with Ollama support for local deployment.
* [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) ⭐ 17,105 | 🐛 538 | 🌐 Python | 📅 2026-03-04 - Open-source, privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
* [DeepCode](https://github.com/HKUDS/DeepCode) ⭐ 16,551 | 🐛 18 | 🌐 Python | 📅 2026-09-17 - Open agentic coding framework that turns papers and specs into working code (Paper2Code, Text2Web, Text2Backend), running against local Ollama or vLLM backends.
* [Trae Agent](https://github.com/bytedance/trae-agent) ⭐ 12,101 | 🐛 163 | 🌐 Python | 📅 2026-02-05 - Privacy-friendly agent framework for orchestrating LLMs and tools, designed for secure, local, and scalable AI workflows.
* [Bytebot](https://github.com/bytebot-ai/bytebot) ⚠️ Archived - A desktop agent is an AI that has its own computer. Unlike browser-only agents or traditional RPA tools, Bytebot comes with a full virtual desktop.
* [AG2](https://github.com/ag2ai/ag2) ⭐ 4,937 | 🐛 27 | 🌐 Python | 📅 2026-09-17 - Open-source operating system for agentic AI with native Ollama support for local model deployment and multi-agent collaboration.
* [agentgateway](https://github.com/agentgateway/agentgateway) ⭐ 4,897 | 🐛 266 | 🌐 Rust | 📅 2026-09-17 - Gateway for managing and orchestrating AI agents with support for local deployment.
* [Orkas](https://github.com/Orkas-AI/Orkas) ⭐ 2,031 | 🐛 12 | 🌐 TypeScript | 📅 2026-09-17 - Open-source, local-first desktop AI workforce whose Commander coordinates specialist agents through one chat; model calls can use a compatible local endpoint.
* [Skales](https://github.com/skalesapp/skales) ⭐ 1,898 | 🐛 4 | 🌐 TypeScript | 📅 2026-09-11 - Source-available (BSL 1.1) local-first desktop AI agent that runs fully on-device, offline via Ollama or with 15+ providers; your files never leave your machine, no cloud required.
* [MFS](https://github.com/zilliztech/mfs) ⭐ 143 | 🐛 3 | 🌐 Python | 📅 2026-07-31 - Exposes your code, docs, chat (Slack/Gmail/Jira), databases and object stores as one file-like, searchable namespace for agents (`ls`/`cat`/`grep` + semantic search); runs fully local with on-device ONNX embeddings on Milvus, no API key.
* [LangChain](https://www.langchain.com/) - Agent and LLM orchestration framework.
* [Haystack](https://haystack.deepset.ai) - End-to-end RAG pipelines.
* [LlamaIndex](https://www.llamaindex.ai) - Data framework for LLM apps.
* [Herdr](https://herdr.dev/) - Self-hosted runtime and terminal multiplexer for coding agents. Runs the agent CLIs on your own machine or a box you control, grouping them into workspaces you can detach from and reattach to over SSH.
* [OpenCode AI](https://opencode.ai/) - Open-source agentic coding platform for private, local, and secure AI-powered development workflows.

## VS Code Plugins & Extensions

> Privacy-first, open-source agentic coding plugins and extensions for VS Code and other editors.

* [cline](https://github.com/cline/cline) ⭐ 68,537 | 🐛 1,352 | 🌐 TypeScript | 📅 2026-09-17 - Privacy-first, open-source agentic coding platform for local AI workflows and automation (VS Code extension).
* [Continue](https://github.com/continuedev/continue) ⭐ 35,946 | 🐛 966 | 🌐 TypeScript | 📅 2026-09-16 - Open-source autocomplete and chat assistant for VS Code and JetBrains, configurable against Ollama, llama.cpp, vLLM, and other local endpoints.
* [Tabby](https://github.com/TabbyML/tabby) ⭐ 33,884 | 🐛 338 | 🌐 Rust | 📅 2026-06-30 - Self-hosted AI coding assistant with its own inference server, offering a private alternative to hosted completion services.
* [Roo Code](https://github.com/RooCodeInc/Roo-Code) ⚠️ Archived - Privacy-first, open-source agentic coding platform for secure, local AI development (VS Code extension).

## Privacy, Security & Governance

> Keep AI deployments secure and compliant.

* [Presidio](https://github.com/microsoft/presidio) ⭐ 10,915 | 🐛 118 | 🌐 Python | 📅 2026-09-17 - Detect and de-identify PII in text and images before it ever reaches a model.
* [garak](https://github.com/NVIDIA/garak) ⭐ 9,288 | 🐛 439 | 🌐 Python | 📅 2026-09-16 - LLM vulnerability scanner that probes local models for prompt injection, jailbreaks, and data leakage.
* [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) ⭐ 7,158 | 🐛 230 | 🌐 Python | 📅 2026-09-17 - Add programmable topical and safety rails to LLM applications, running alongside self-hosted models.
* [LLM Guard](https://github.com/protectai/llm-guard) ⚠️ Archived - Input and output scanning toolkit covering prompt injection, PII, toxicity, and secrets leakage.
* [Concrete](https://github.com/zama-ai/concrete) ⭐ 1,576 | 🐛 57 | 🌐 C++ | 📅 2025-12-19 - Fully homomorphic encryption for AI.
* [OpenFL](https://github.com/securefederatedai/openfl) ⭐ 843 | 🐛 83 | 🌐 Python | 📅 2026-08-25 - Federated learning framework.
* [BlindAI](https://github.com/mithril-security/blindai) ⭐ 512 | 🐛 6 | 🌐 Rust | 📅 2024-03-19 - Confidential AI inference using TEEs.
* [Flower](https://flower.dev) - Federated learning at scale.

## Observability & Evaluation

> Measure and monitor private deployments without shipping traces to a vendor.

* [Langfuse](https://github.com/langfuse/langfuse) ⭐ 34,733 | 🐛 908 | 🌐 TypeScript | 📅 2026-09-17 - Self-hostable LLM observability, tracing, prompt management, and evaluation.
* [promptfoo](https://github.com/promptfoo/promptfoo) ⭐ 25,234 | 🐛 629 | 🌐 TypeScript | 📅 2026-09-17 - Local-first evaluation and red-teaming for prompts and models, runnable entirely offline in CI.
* [DeepEval](https://github.com/confident-ai/deepeval) ⭐ 18,313 | 🐛 613 | 🌐 Python | 📅 2026-09-16 - Unit-testing framework for LLM outputs, with metrics that can run against locally hosted judge models.
* [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) ⭐ 14,013 | 🐛 985 | 🌐 Python | 📅 2026-09-14 - The standard harness for benchmarking language models, supporting local vLLM and Hugging Face backends.
* [Phoenix](https://github.com/Arize-ai/phoenix) ⭐ 11,519 | 🐛 1,011 | 🌐 Python | 📅 2026-09-17 - Self-hosted tracing, evaluation, and experiment tracking for LLM applications.
* [OrcaReplay](https://github.com/Continuum-AI-Corp/OrcaReplay) ⭐ 254 | 🐛 8 | 🌐 TypeScript | 📅 2026-09-17 - Records an agent at the HTTP boundary and serves the recording back, so a run reproduces with the model server switched off; traces are files in the project and nothing is uploaded.

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

* [Open WebUI](https://github.com/open-webui/open-webui) ⭐ 152,401 | 🐛 299 | 🌐 Python | 📅 2026-09-17 - Commonly recommended Web UI frontend which features built in search, web scrape, RAG, and optional user authentication.
* [Lobe Chat](https://github.com/lobehub/lobe-chat) ⭐ 82,549 | 🐛 918 | 🌐 TypeScript | 📅 2026-09-17 - Modern self-hosted chat framework with plugin and multimodal support, deployable in one click against local backends.
* [text-generation-webui](https://github.com/oobabooga/text-generation-webui) ⭐ 47,680 | 🐛 839 | 🌐 Python | 📅 2026-08-17 - Long-standing Gradio web UI for local text generation, supporting llama.cpp, ExLlama, and transformers backends.
* [LibreChat](https://github.com/danny-avila/LibreChat) ⭐ 44,232 | 🐛 754 | 🌐 TypeScript | 📅 2026-09-17 - Enhanced web UI for LLMs.
* [SillyTavern](https://github.com/SillyTavern/SillyTavern) ⭐ 33,486 | 🐛 619 | 🌐 JavaScript | 📅 2026-09-14 - Self-hosted, highly customizable frontend for local models, with extensive character, prompt, and context management.
* [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) ⭐ 33,352 | 🐛 242 | 🌐 TypeScript | 📅 2024-08-03 - Open-source ChatGPT clone.
* [Screenpipe](https://github.com/screenpipe/screenpipe) ⭐ 21,609 | 🐛 53 | 🌐 TypeScript | 📅 2026-09-17 - 24/7 local screen + microphone recording with OCR, audio transcription, and semantic search. Fully offline with Ollama or any local LLM. MCP server for Claude.
* [AnythingLLM](https://anythingllm.com/) - Full-stack private LLM workspace.

## Image & Video Generation

> Run diffusion and video models on your own GPUs.

* [AUTOMATIC1111 Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) ⭐ 164,995 | 🐛 2,505 | 🌐 Python | 📅 2026-03-02 - The most widely deployed self-hosted Stable Diffusion interface, with a large extension ecosystem.
* [ComfyUI](https://github.com/comfyanonymous/ComfyUI) ⭐ 133,677 | 🐛 4,886 | 🌐 Python | 📅 2026-09-17 - Node-based interface and backend for diffusion models, running image, video, and audio pipelines entirely locally.
* [InvokeAI](https://github.com/invoke-ai/InvokeAI) ⭐ 28,236 | 🐛 371 | 🌐 Python | 📅 2026-09-15 - Professional-grade local generative image toolkit with a unified canvas and workflow editor.

## Speech & Audio

> Private speech-to-text and text-to-speech.

* [Whisper](https://github.com/openai/whisper) ⭐ 109,291 | 🐛 149 | 🌐 Python | 📅 2026-08-31 - The original open-weight speech recognition model, runnable fully offline.
* [whisper.cpp](https://github.com/ggml-org/whisper.cpp) ⭐ 53,731 | 🐛 351 | 🌐 C++ | 📅 2026-09-15 - C++ port of OpenAI's Whisper automatic speech recognition model, optimized for local, CPU/GPU inference without internet connectivity.
* [WhisperX](https://github.com/m-bain/whisperX) ⭐ 24,084 | 🐛 223 | 🌐 Python | 📅 2026-08-30 - Whisper with word-level timestamps, speaker diarization, and much faster batched transcription.
* [F5-TTS](https://github.com/SWivid/F5-TTS) ⭐ 15,240 | 🐛 62 | 🌐 Python | 📅 2026-07-23 - Local text-to-speech with voice cloning from a short reference sample.
* [RealtimeSTT](https://github.com/KoljaB/RealtimeSTT) ⭐ 10,137 | 🐛 148 | 🌐 Python | 📅 2026-09-17 - Low-latency local speech-to-text with voice activity detection, for building private voice interfaces.
* [speaches](https://github.com/speaches-ai/speaches) ⭐ 3,666 | 🐛 146 | 🌐 Python | 📅 2026-09-17 - Self-hosted OpenAI-compatible server for transcription, translation, and speech generation.

## Datasets & Data Prep

> Create and manage private training corpora.

* [MinerU](https://github.com/opendatalab/MinerU) ⭐ 80,110 | 🐛 113 | 🌐 Python | 📅 2026-09-17 - High-quality PDF-to-Markdown and JSON extraction, including formulas and tables, for building private corpora.
* [Docling](https://github.com/docling-project/docling) ⭐ 66,569 | 🐛 909 | 🌐 Python | 📅 2026-09-17 - Parse PDF, DOCX, PPTX, and HTML into structured formats for RAG and training, running entirely on your own hardware.
* [Marker](https://github.com/datalab-to/marker) ⭐ 39,815 | 🐛 471 | 🌐 Python | 📅 2026-09-13 - Fast, accurate document-to-Markdown conversion across PDFs, images, and office formats.
* [Label Studio](https://github.com/HumanSignal/label-studio) ⭐ 28,288 | 🐛 947 | 🌐 TypeScript | 📅 2026-09-17 - Self-hosted data labelling platform for text, image, audio, and video annotation.
* [Unstructured](https://github.com/Unstructured-IO/unstructured) ⭐ 15,444 | 🐛 309 | 🌐 HTML | 📅 2026-09-15 - Ingestion and preprocessing library for turning messy documents into model-ready chunks.
* [Argilla](https://github.com/argilla-io/argilla) ⭐ 5,109 | 🐛 34 | 🌐 Python | 📅 2026-09-14 - Collaborative tool for curating, annotating, and quality-checking datasets for fine-tuning and evaluation.
* [OpenWebText](https://skylion007.github.io/OpenWebTextCorpus/) - Open dataset similar to GPT training data.
* [RedPajama](https://www.together.xyz/blog/redpajama) - Open LLM training dataset.

## Learning Resources & Research

> Guides, papers, and tutorials on private AI.

* [LLMs from Scratch](https://github.com/rasbt/LLMs-from-scratch) ⭐ 105,155 | 🐛 2 | 🌐 Jupyter Notebook | 📅 2026-09-17 - Build a GPT-style model step by step in PyTorch, on your own machine.
* [LLM Course](https://github.com/mlabonne/llm-course) ⭐ 83,002 | 🐛 90 | 📅 2026-02-05 - Roadmap and notebooks covering LLM fundamentals, fine-tuning, quantization, and deployment.
* [ML Engineering Open Book](https://github.com/stas00/ml-engineering) ⭐ 19,008 | 🐛 4 | 🌐 Python | 📅 2026-09-12 - Field-tested notes on training and serving large models: hardware, parallelism, throughput, and debugging.
* [Smol Course](https://github.com/huggingface/smol-course) ⭐ 6,745 | 🐛 98 | 🌐 Jupyter Notebook | 📅 2026-09-17 - Hugging Face's practical course on aligning and fine-tuning small models that fit on local hardware.

## AI Routers & API Aggregators

> Centralized routers and proxy layers for aggregating, governing, and securing your private AI stack. These tools simplify connections to multiple model servers, optimize LLM routing, and provide observability, security, and compliance.

* [LiteLLM](https://github.com/BerriAI/litellm) ⭐ 59,013 | 🐛 5,202 | 🌐 Python | 📅 2026-09-17 - Self-hosted proxy exposing 100+ model backends — including Ollama, vLLM, and any OpenAI-compatible server — behind one API, with keys, budgets, routing, and logging.
* [Bifrost](https://github.com/maximhq/bifrost) ⭐ 8,144 | 🐛 1,057 | 🌐 Go | 📅 2026-09-17 - Self-hosted, open-source AI gateway for multi-provider routing, failover, observability, guardrails, and budget controls.
* [Nexus](https://github.com/grafbase/nexus) ⭐ 436 | 🐛 28 | 🌐 Rust | 📅 2026-03-16 - Open-source AI router to aggregate Model Context Protocol (MCP) servers, intelligently route requests to the best LLMs, and provide security, governance, observability, and simplified architecture for private AI deployments. [Blog](https://nexusrouter.com/blog/introducing-nexus-the-open-source-ai-router)

## Contributing

Contributions welcome! See [Contributing](CONTRIBUTING.md)

## License

Under CC0-1.0 license. see [LICENSE](LICENSE)

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-09-17._
