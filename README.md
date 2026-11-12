# Awesome Decisions API [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Models and APIs that *pick* — choice, score, or yes/no with a probability — instead of writing chat. TypeSafe Jev opened the category; OpenAI, Cloudflare, Perplexity, and others shipped peers in late September and early October 2026.

## Contents

- [Official Resources](#official-resources)
- [Models](#models)
- [Gateways](#gateways)
- [SDKs](#sdks)
- [Runtimes](#runtimes)
- [Articles and Press](#articles-and-press)
- [Related](#related)

## Official Resources

- [Introducing System One and Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev) - TypeSafe announcement of the decision-model category and Jev. Direct API, not a gateway.
- [Jev 1.14 Release](https://typesafe.ai/blog/jev-1-14) - TypeSafe post releasing `jev-1.14.0` with experimental image input, a `box` question type that returns a bounding box, and opt-in long context.

## Models

- [TypeSafe Jev](https://docs.typesafe.ai/models) - Text-only Choice, Score, and Noul with calibrated probabilities. Generally available; about $0.042 per million input tokens.
- [Cloudflare Clef and Clef-flash](https://blog.cloudflare.com/clef-decision-models/) - Jev-API compatible, vision, 64k context, Apache-2.0 weights, Workers AI, and RL fine-tune.
- [Perplexity pplx-decider-v1-27b](https://huggingface.co/perplexity-ai/pplx-decider-v1-27b) - Multimodal open weights. Hosted Decisions API about $0.04 per million input tokens. Perplexity reports it ahead of Jev on their 11-benchmark panel.
- [Strands Decider 2B](https://strandsagents.com/blog/introducing-strands-decider/) - AWS Strands Labs open-source 2B decision model (Choice, Noul, Score). Weights on [Hugging Face](https://huggingface.co/StrandsAgents/strands-decider-2B-hobson-v19); code at [strands-labs/strands-decider](https://github.com/strands-labs/strands-decider).
- [Inception Mercury Decide](https://openrouter.ai/inception/mercury-decide:free) - System One-shaped decision model (`inception/mercury-decide:free`). Text in; choice, score, or yes/no with a probability.
- [LiquidAI D1](https://docs.liquid.ai/lfm/models/decision-models) - Purpose-built models for classification, routing, and scoring in one call, with no generated tokens. Hosted as `liquid/d1`.
- [Kev](https://github.com/jaredpalmer/kev) - Open-weight Jev-compatible family (Apache-2.0) with a local `/v1/systemone` server. Announcement: [Introducing Kev](https://jaredpalmer.com/blog/introducing-kev).
- [meraGPT Decider 1](https://meragpt.com/docs) - System One decision endpoint on the meraGPT API.
- [Solar Decide](https://openrouter.ai/upstage/solar-decide) - Upstage structured decision model on Solar Mini 4, served as a System One endpoint. About $0.05 per million input tokens.
- [Nimble](https://github.com/bespokelabsai/nimble) - Local typed decisions, plus contrastive data curation and model evaluation.
- [Tev1](https://huggingface.co/togethercomputer/Tev1-4B-experimental) - Together experimental fine-tune of Qwen3.5-4B that picks one option from a state, a question, and a list of choices.
- [Laya](https://github.com/NandhaKishorM/laya) - Non-autoregressive System One engine for typed choice, score, and yes/no over text in one forward pass.
- [Jeeves](https://github.com/PostHog/jeeves) - PostHog open 9B Jev-like model (MIT) that reasons before it decides, answering choice, score, and yes/no questions through a Jev-compatible API.
- [TokenAI Neo](https://tokenai.llc/models/neo) - Open-weights 41M-parameter encoder decision model with choice, score, and noul heads that flags low-confidence tool routing for review. Custom TokenAI license.
- [Wald-Q4B](https://huggingface.co/org2ai/Wald-4B) - Open-weight 4B decision model (Apache-2.0) built on Qwen3.5-4B-Base that returns a calibrated probability for every option through a Jev-compatible `/v1/systemone` API.
- [gutsy](https://github.com/kouhxp/gutsy) - Local 0.8B decision model (Apache-2.0), a Qwen3.5-0.8B fine-tune that runs on CPU through llama.cpp and answers yes/no, choice, and score questions through a Jev-style API.
- [Databricks ai_decide](https://docs.databricks.com/aws/en/sql/language-manual/functions/ai_decide) - Beta Databricks AI Function that answers `noul`, `choice`, and `score` questions over text or structured data in SQL, returning a probability, a named choice, or a score on an ordered scale.
- [Decision Models](https://decisionmodels.io/) - Hosted Jev-compatible API, formerly System1 Models, that serves the open-weight decision models `s1-fast`, `s1-pro`, and `s1-vision`, with an optional EU-hosted tier.
- [SubQ Snap](https://subq.ai/introducing-subq-snap) - Subquadratic long-context decision model (`subq-snap-preview`) with up to 384K tokens of text and images, served at `/v1/systemone` with noul, choice, and score questions. About $0.05 per million input tokens, output free.
- [Microsoft-Decision-1](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/how-to/use-foundry-models-microsoft-decision) - Microsoft Foundry decision model for classification, routing, ranking, and grading that returns `noul`, `choice`, and `score` answers from a `/v1/systemone` endpoint.
- [OpenAI Decisions API](https://developers.openai.com/api/docs/guides/decisions) - Public beta `POST /v1/decisions` endpoint on `gpt-6-luna` for predicate, choice, and score questions over text and images. Input-only pricing at $0.10 per million tokens.
- [H2O-Lightning-4B](https://huggingface.co/h2oai/h2o-lightning-4b) - H2O.ai open-weight 4B decision model (Apache-2.0) built on Qwen3.5-4B that answers choice, yes/no, and score questions about text and images through a `/v1/systemone` API.
- [Decision 3.0](https://huggingface.co/collections/vllm-sr/decision-30-6aca5f47b0d942380f6e4a64) - vLLM Semantic Router family of six Apache-2.0 multimodal decision models, from d3-edge to the 27B d3, that answer Choice, Yes/No, and Score questions over text, images, and video with a probability for every answer.
- [OneJev](https://github.com/OmniJev/OneJev) - Apache-2.0 multimodal System One decision model on Qwen in 0.8B, 4B, 9B, and 27B sizes that returns calibrated probabilities for typed questions about screenshots, photos, videos, and text through a TypeSafe System One-compatible API.
- [RSI-Jev](https://github.com/Shanghua-Gao/RSI-Jev) - Jev-style decision models built by a self-improving loop of AI agents that publishes every experiment, failures included, with Apache-2.0 weights and a Jev-compatible `/v1/systemone` server.
- [OpenJev](https://huggingface.co/openjev/openjev) - Open-weights 27B decision model that answers choice, yes/no, and score questions about text, web pages, and screenshots through a Jev-compatible `/v1/systemone` API. CC BY-NC 4.0 weights.
- [AutoTrust JEV](https://huggingface.co/autotrust/JEV-9B) - Open Apache-2.0 family (JEV-9B and JEV-27B) that serves calibrated System 1 decisions (`noul`, `choice`, `score`) and System 2 generation from one set of weights through a `/v1/decide` endpoint.
- [Julia 1](https://supersoniclabs.ai/julia-1/) - Compact 144M multilingual decision model (Apache-2.0) built on mmBERT-small that classifies, ranks ordered levels, and answers yes-or-no questions among supplied options, including on CPU.
- [Open-Jev](https://zefan-cai.github.io/open-jev/) - Open family of LoRA decision adapters (2B, 9B, and 27B) over Qwen that return typed Choice, Noul, and Score probabilities through a `/v1/systemone` server.
- [Jebadiah v2.1](https://huggingface.co/blog/frontier-infra/jebadiah-v2-1) - Open decision models in 9B and 27B (Apache-2.0) with GGUF and MLX builds, answering typed questions with a pick and a confidence in a single pass.
- [Lumma-Fev-27B](https://huggingface.co/blog/FrontiersMind/lumma-fev-27b) - FrontiersMind 27B decision model (Apache-2.0) on the same `/v1/systemone` contract as Jev, trained on `noul` and `choice` questions in English, Hindi, Tamil, and Kannada.
- [Drex Max](https://console.nace.ai/docs/drex/guides/drex-max) - Nace multimodal decision model on a Jev-style `/v1/systemone` endpoint that reads text and images and answers yes/no, choice, and score questions. About $0.06 per million input tokens.
- [Celeris-1 Decision](https://celeris.ai/celeris-1-decision) - Hosted diffusion decision model for yes/no, choice, and score questions over text, structured data, or images, with an optional one-sentence explanation. About $0.04 per million input tokens.
- [Cloudflare Clef-omni](https://blog.cloudflare.com/clef-faster-cheaper-multimodal/) - Open-weight Clef decision model on Workers AI that takes audio, video, image, and text in one call. About $0.15 per million input tokens.
- [Sqwish kettei](https://sqwish.ai/onehot) - Sqwish Labs decision models in four sizes that give each allowed answer a probability, with multimodal fat and chub and open-weight core and dot.
- [Liquid AI open d1](https://huggingface.co/blog/LiquidAI/open-d1) - Open-weight d1-3B (text and images) and experimental d1-omni-600M (text with images or audio) decision models built for edge devices.
- [ToddlerJev](https://teenage.works/blog/toddler-jev) - Open-weight native-audio decision model from TeenageWorks that assigns a probability to each request-time candidate in one forward pass, without transcription.
- [Liquid d1-ultra](https://www.liquid.ai/blog/d1-ultra) - Liquid AI multimodal decision model that reads text, images, or both and returns noul, choice, and score probabilities in one forward pass with no generated tokens. About $0.042 per million input tokens on the Liquid API.
- [Base Labs mammoth-1 and elephant-1](https://labs.baseten.co/articles/mammoth-1-and-elephant-1-frontier-decision-models) - Open-weight 27B and 9B decision models post-trained from Qwen3.5 with block-bidirectional attention, with weights released on Hugging Face.
- [THX-01](https://huggingface.co/blog/doofz/thx-01-we-open-sourced-a-322m-decision-model-that) - HAL-X AI open-source 322M multilingual decision model under Apache-2.0, with one-pass calibrated probabilities, document extraction, and a free hosted API with usage limits.
- [Alibaba Cloud Decision Model](https://www.alibabacloud.com/help/en/model-studio/decision-model-api) - Bailian `decision-model-preview` on Model Studio's `POST /compatible-mode/v1/systemone` endpoint, returning choice, score, and yes/no answers with full probability distributions in one forward pass without generating text.
- [OpenDecider-nano](https://huggingface.co/manjunathshiva/opendecider-nano) - Open ~400M encoder decision model (Apache-2.0) that answers choice, score, and yes/no questions with a calibrated probability for every option in one forward pass.
- [Decision-2.0-Nox-4B](https://huggingface.co/vllm-sr/Decision-2.0-Nox-4B) - vLLM Semantic Router 4B decision model (Apache-2.0) that answers choice, yes/no, and score questions together with a probability for every answer.
- [Quyet-1.0-Tiny](https://huggingface.co/chinhnc/Quyet-1.0-Tiny) - Compact 183M decision model (Apache-2.0) on mmBERT-small, tuned for English and Vietnamese, that returns calibrated probabilities in the `/v1/systemone` answer shape.
- [CoCo-Decision-4B](https://huggingface.co/corners-ai/CoCo-Decision-4B) - Text-only 4B decision model on Qwen3.5-4B that returns a probability distribution for yes/no, choice, and score questions.
- [Hume Audio Decision API](https://www.hume.ai/blog/introducing-hume-audio-decision-api) - Audio-native decision model that answers yes/no, choice, scale, and span questions about speech and sound, returning probabilities over the answers you define.
- [Kanana-2-v-decide-3b-2611](https://huggingface.co/kakaocorp/kanana-2-v-decide-3b-2611) - Kakao's 3B multimodal decision model that answers choice, noul, and score questions with a probability for each answer, and ships a System One-compatible HTTP server.
- [Pea](https://itsvej.com/journal/pea-decisions-launch/) - Vej's 2B text decision model that returns a probability for every choice, noul, or score outcome, with hosted early access and gated open weights.
- [Torchcast Decision 4B](https://huggingface.co/torchcast-ai/torchcast-decision-4b) - Open-weight decision model (Apache-2.0) fine-tuned from Qwen3.5-4B that returns yes/no, choice, and score distributions in one forward pass through a TypeSafe-compatible API and a bundled server.
- [Gemini Decision 1](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/) - Google multimodal decision model behind the Gemini Decisions API, answering up to 1,000 yes/no, choice, and score questions per request with a confidence on every answer.

## Gateways

- [OpenRouter Decisions](https://openrouter.ai/docs/guides/community/jev) - Jev via `/api/alpha/decisions` and `/api/v1/systemone`.
- [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - `typesafe-ai/jev` through the AI SDK `evaluate` helper.
- [Cloudflare Workers AI](https://developers.cloudflare.com/ai/models/typesafe/jev/) - `typesafe/jev` on the Workers AI binding. Clef is on the same binding; its model page is under Models.
- [Decisions API Workbench](https://decisions-api.dev/docs) - Independent playground and API service exposing many decision models, including Jev, Liquid d1, Solar Decide, Perplexity Decider, and Cloudflare Clef, behind one System One endpoint with credit-based billing.
- [LiteLLM Decisions](https://docs.litellm.ai/docs/decisions) - Proxy routes `POST /v1/decisions` and `POST /v1/systemone` that translate between OpenAI Decisions and System One formats across providers such as OpenAI, TypeSafe Jev, Perplexity, Cloudflare Clef, and self-hosted vLLM.
- [AI/ML API Decision Models](https://docs.aimlapi.com/api-references/decision-models) - TypeSafe Jev 1.14 and 1.13 alongside Liquid AI and OpenAI decision models on the AI/ML API.
- [TrueFoundry AI Gateway](https://www.truefoundry.com/blog/blog-decisions-api-is-now-live-on-truefoundry-ai-gateway) - Serves decision models on both `POST /v1/decisions` and `POST /v1/systemone`, translating between the OpenAI and System One formats across seven providers.
- [OpenAI Decisions on Vercel AI Gateway](https://vercel.com/changelog/openai-decisions-api-now-available-on-ai-gateway) - Vercel changelog adding the OpenAI-format `/v1/decisions` endpoint to AI Gateway, with `openai/gpt-6-luna-decisions` and other decision models.
- [AnyRouter Decisions](https://blog.anyrouter.dev/releases/2026-10-10-decisions) - AnyRouter release adding Microsoft-Decision-1, Solar Decide Flash, PPLX Decider v1.1, Drex v1.5, and SubQ Snap Preview behind one `POST /api/v1/decisions` contract.
- [TrustedRouter Decide](https://aws.trustedrouter.com/docs/decide) - Attested gateway with `POST /api/alpha/decide` for boolean, choice, and score questions across tuned decision configurations and chat models.
- [Triton AI Decisions](https://docs.tritonai.ucsd.edu/llm-api/decisions) - UC San Diego API offering a beta decisions model through both the OpenAI Decisions format and the SystemOne format.
- [Vercel AI Gateway Gemini Decision 1](https://vercel.com/changelog/gemini-decision-1-now-available-on-ai-gateway) - Gemini Decision 1 as `google/gemini-decision-1` through the AI SDK and the `/v1/decisions` endpoint.

## SDKs

- [TypeSafe Python SDK](https://github.com/typesafe-ai/typesafe-sdk-python) - Official Python library for the TypeSafe API.
- [TypeSafe JavaScript SDK](https://github.com/typesafe-ai/typesafe-sdk-js) - Official TypeScript and JavaScript library for the TypeSafe API.
- [AnyDecisionModel](https://github.com/mattt/AnyDecisionModel) - Apache-2.0 Swift package for typed yes/no, choice, and score decisions with probabilities, backed by local MLX, Core AI, or llama.cpp models, Clef decision heads, Jev, or Ollama.
- [decision-pony](https://github.com/CyanSalt/decision-pony) - TypeScript library that converts OpenAI Decisions API requests to Chat Completions, Responses, or Anthropic Messages requests and back so those APIs can act as a Decisions polyfill, and also converts to and from the TypeSafe Jev API.

## Runtimes

- [Ollama decision models](https://ollama.com/blog/ollama-now-supports-jev-style-decision-models) - Local Jev-style choice, score, and yes/no, with a probability on every option.
- [OpenRouter decisions filter](https://openrouter.ai/models?output_modalities=decisions) - Catalog filtered to models with decision output.
- [Bud Decision Studio](https://github.com/BudEcosystem/Bud-Decision-Studio) - Desktop app and local server for running open Jev-like decision models on macOS, Windows, and Linux, returning a calibrated probability for every answer.
- [ollaya](https://github.com/ollaya-dev/ollaya) - Local daemon that pulls open decision models such as Laya by name and serves them behind TypeSafe's `/v1/systemone` wire format, the way Ollama runs LLMs.
- [vLLM Jev](https://github.com/mode-io/vllm-jev) - Native vLLM serving for Jev-style decision models on Linux, with an Apple Silicon preview, answering Choice, Noul, and Score requests at `/v1/systemone`.
- [AnyJev](https://github.com/nokia-applied-research/AnyJev) - Nokia Applied Research library (Apache-2.0) that turns an existing LLM into a Jev-style decision model with a training-free readout, plus self-distilled Tacit models from 1.7B to 9B.
- [llama.cpp decision models](https://huggingface.co/blog/ggml-org/decision-models-in-llamacpp) - Local `/v1/systemone` endpoint in the llama.cpp server for Jev-style choice, score, and noul questions, with GGUF builds of models such as Julia-1, Laya, Kev-4B, and OpenJev.
- [vLLM Structured Decisions Models](https://docs.vllm.ai/en/latest/models/structured_decisions_models/) - vLLM docs for its text-only implementation of OpenAI's `POST /v1/decisions` API on self-served models.
- [DecisionFormer](https://huggingface.co/blog/FrontiersMind/decisionformer) - FrontiersMind open-source library for fine-tuning any Hugging Face model into a calibrated one-pass decision model with full fine-tuning, LoRA, or QLoRA, and serving it as an API.

## Articles and Press

- [OpenAI’s Jev clone](https://techcrunch.com/2026/09/30/openais-jev-clone-could-help-the-frontier-lab-stop-its-swarming-agents/) - TechCrunch on the Decisions API at DevDay. Luna-based, limited preview, vision claimed. No public docs page yet, so this is the citation.
- [DevDay 2026 recap](https://openai.com/index/devday-2026-recap) - OpenAI’s own recap of DevDay 2026, beside the TechCrunch piece.
- [Amazon releases its own Jev clone](https://techcrunch.com/2026/10/01/amazon-releases-its-own-jev-clone-as-decision-models-flood-the-web/) - TechCrunch on Strands Decider 2B.
- [Cloudflare announcement](https://x.com/Cloudflare/status/2105747536510099540) - Birthday Week post for Clef. Swap for a docs URL when one exists.
- [Perplexity Decisions quickstart](https://docs.perplexity.ai/docs/decisions/quickstart) - Official Decisions API quickstart, in place of the launch post.
- [Perplexity follow-up](https://x.com/AravSrinivas/status/2106119404433908149) - Follow-up on the decider versus Jev.
- [How to classify, route, and score with Jev and AI SDK](https://vercel.com/kb/guide/typesafe-jev-and-ai-sdk) - Vercel guide to typed Jev answers through the AI SDK `experimental_evaluate` API and AI Gateway.
- [How to Use Jev: Moderation with the Jev API in TypeScript](https://openrouter.ai/blog/tutorials/how-to-use-jev/) - OpenRouter tutorial building a marketplace listing moderation check from choice, yes/no, and score questions.
- [LLM2Jev](https://arxiv.org/abs/2610.02076) - Paper from Microsoft researchers showing general-purpose LLMs already work as Jev-style decision models out of the box, with a training-free readout and a KL-anchored fine-tuning recipe.
- [Jev for Python engineers](https://vercel.com/blog/jev-for-python-engineers) - Vercel post introducing the experimental `evaluate()` API in the AI SDK for Python, with `ChoiceQuestion`, `ScoreQuestion`, and `NoulQuestion` types, published October 2026.
- [The First Open-Weight Alternatives to Jev](https://whitepapers.aetherix.com/papers/jev-open-weight-alternatives/) - Aetherix white paper comparing six open-weight decision models on one NVIDIA DGX Spark with a shared 25-question smoke test, published October 2026.
- [General Decision Models: Benchmarking and Insights Beyond Jev](https://arxiv.org/abs/2610.03935) - Paper introducing JEVal, a bilingual benchmark of 11,257 instances across 36 datasets, and the InnerJev-4B and InnerJev-27B decision models.
- [Decision model benchmark: Jev, Kev, Liquid d1, and more](https://arize.com/blog/decision-model-benchmark/) - Arize benchmark of eight decision models on hallucination detection, Phoenix evaluator suites, and agent routing, showing that rewording a question flips several models' answers, published October 2026.
- [Jev 1.14 on AI Gateway](https://vercel.com/changelog/typesafe-ais-jev-1-14-is-now-available-on-ai-gateway) - Vercel changelog adding `typesafe-ai/jev-1.14.0` to AI Gateway, with image input and an experimental long-context mode, published October 15, 2026.
- [AI Decision Models Compared](https://www.techfabric.com/blog/ai-decision-models-compared-jev-clef-kev-microsoft) - TechFabric comparison of TypeSafe Jev, Cloudflare Clef, Kev, and Microsoft-Decision-1, published October 2026.
- [Meet Drex Max](https://www.marktechpost.com/2026/10/19/nace-ai-drex-max-multimodal-decision-model/) - MarkTechPost on Nace's multimodal decision model for computer-use agents and its reported 67.59 on Decision Index 0.3.2.
- [StructuredAI can now ask Jev, OpenAI Decisions and Mercury Decide](https://blog.curiosity.ai/blog/2026-10-structured-ai-decision-providers) - Curiosity post on sending one set of typed questions to Jev, OpenAI Decisions, or Mercury Decide, with a comparison of their formats and prices.
- [How to Use the OpenAI Decisions API](https://apidog.com/blog/how-to-use-openai-decisions-api/) - Apidog walkthrough of first calls in curl, Python, and JavaScript, the predicate, choice, and score answer types, and image input.
- [Decision Tier](https://robgruhl.github.io/jev-learnings/) - Tutorial site drawn from two projects that use Jev as a cheap, fast judgment tier between deterministic code and an expensive LLM, running from ELI5 to engineering.
- [Build More Responsive Apps with the Decisions API](https://openai.com/index/decisions-api) - OpenAI announcement of general availability for the GPT-6 Luna Decisions API, with up to 400 questions per request, prompt caching, and US and EU residency.
- [Microsoft-Decision-1 Explained](https://wilsonwu.me/blog/2026/microsoft-decision-1/) - Wilson Wu's comparison of Microsoft-Decision-1 with Jev and Laya, covering architecture, API compatibility, official benchmarks, and JevBench results.
- [OpenAI makes its Jev competitor widely available](https://techcrunch.com/2026/10/22/openai-makes-its-jev-competitor-widely-available-as-decision-model-competition-heats-up/) - TechCrunch on the Decisions API becoming available to all OpenAI customers on October 22, 2026, with voice and visual modalities added.
- [Jev question types: Choice, Score and Noul](https://madewithjev.com/jev-question-types) - Reference guide to the three Jev question types and what each one returns.
- [JevMan](https://opper.ai/jevman-benchmark/) - Opper AI open-source Pac-Man benchmark where each decision model plays 100 real-time games, returning a probability per direction at every junction.
- [OpenAI Decisions API: Price, Question Types, vs Jev](https://cellcog.ai/blog/openai-decisions-api/) - CellCog breakdown of the Decisions API from beta to general availability, its predicate, choice, and score questions, and pricing against Jev.
- [Decision Model API: 7 Vendors, Prices and How to Choose](https://jev101.org/decision-model-api) - Comparison of hosted and open-weight decision models by price, question types, vision input, and deployment.
- [The Enterprise AI Push For Decision Models](https://inc42.com/features/the-enterprise-ai-push-for-decision-models/) - Inc42 feature on enterprise interest in decision models that return scores and yes/no probabilities rather than generated text.
- [Web grounding for the Decisions API](https://www.perplexity.ai/hub/blog/web-grounding-for-the-decisions-api) - Perplexity post adding a `web_grounding` mode that runs a search per question and appends the results as evidence, with reported PWS-Decisions accuracy rising from 51% to 86%, published November 2026.
- [Meet Koa Decisions](https://www.salesforce.com/news/stories/koa-decisions-salesforce-decision-models/) - Salesforce announcement of Koa Decisions, the successor to its HyperClassifier routing model, built on Gemma, with a planned developer API.
- [What Is a Decisions API?](https://parallel.ai/articles/what-is-a-decisions-api) - Parallel explainer covering the three question types, the two main request shapes, a provider and pricing table, and when web-grounded decisions help.
- [Decision Models in Hugging Face](https://huggingface.co/blog/decision) - Hugging Face post introducing the Transformers `decision` pipeline, `AutoModelForDecision`, `/v1/systemone` serving in Transformers and llama.cpp, the Hub `decision-model` tag, and fine-tuning with `Trainer`, published November 10, 2026.
- [How to Use the Gemini Decisions API](https://flaviocopes.com/gemini-decisions-api/) - Flavio Copes tutorial calling Gemini Decision 1 from Node.js with `noul`, `choice`, and `score` questions and branching on the probabilities.

## Related

- [Awesome Claude Managed Agents](https://github.com/paulmeller/awesome-managed-agents) - Curated list for Anthropic’s managed agent runtime.
- [Awesome Agent Client Protocol](https://github.com/paulmeller/awesome-agent-client-protocol) - Curated list for ACP.

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.
