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

## Gateways

- [OpenRouter Decisions](https://openrouter.ai/docs/guides/community/jev) - Jev via `/api/alpha/decisions` and `/api/v1/systemone`.
- [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - `typesafe-ai/jev` through the AI SDK `evaluate` helper.
- [Cloudflare Workers AI](https://developers.cloudflare.com/ai/models/typesafe/jev/) - `typesafe/jev` on the Workers AI binding. Clef is on the same binding; its model page is under Models.

## SDKs

- [TypeSafe Python SDK](https://github.com/typesafe-ai/typesafe-sdk-python) - Official Python library for the TypeSafe API.
- [TypeSafe JavaScript SDK](https://github.com/typesafe-ai/typesafe-sdk-js) - Official TypeScript and JavaScript library for the TypeSafe API.

## Runtimes

- [Ollama decision models](https://ollama.com/blog/ollama-now-supports-jev-style-decision-models) - Local Jev-style choice, score, and yes/no, with a probability on every option.
- [OpenRouter decisions filter](https://openrouter.ai/models?output_modalities=decisions) - Catalog filtered to models with decision output.

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

## Related

- [Awesome Claude Managed Agents](https://github.com/paulmeller/awesome-managed-agents) - Curated list for Anthropic’s managed agent runtime.
- [Awesome Agent Client Protocol](https://github.com/paulmeller/awesome-agent-client-protocol) - Curated list for ACP.

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.
