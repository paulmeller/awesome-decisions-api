# Awesome Decisions API [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Models and APIs that *pick* — choice, score, or yes/no with a probability — instead of writing chat. TypeSafe Jev opened the category; OpenAI, Cloudflare, Perplexity, and others shipped peers in late September and early October 2026.

## Contents

- [Official Resources](#official-resources)
- [Models](#models)
- [Gateways](#gateways)
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
- [LiquidAI D1](https://openrouter.ai/liquid/d1) - Hosted System One-shaped decision model. OpenRouter lists about $0.04 per million input tokens and free output.
- [Kev](https://github.com/jaredpalmer/kev) - Open-weight Jev-compatible family (Apache-2.0) with a local `/v1/systemone` server. Announcement: [Introducing Kev](https://jaredpalmer.com/blog/introducing-kev).

## Gateways

- [OpenRouter Decisions](https://openrouter.ai/docs/guides/community/jev) - Jev via `/api/alpha/decisions` and `/api/v1/systemone`.
- [Vercel AI Gateway](https://vercel.com/changelog/typesafe-ai-jev-now-available-on-ai-gateway) - `typesafe-ai/jev` through the AI SDK `evaluate` helper.
- [Cloudflare Workers AI](https://developers.cloudflare.com/ai/models/typesafe/jev/) - `typesafe/jev` on the Workers AI binding. Clef is on the same binding; its model page is under Models.

## Articles and Press

- [OpenAI’s Jev clone](https://techcrunch.com/2026/09/30/openais-jev-clone-could-help-the-frontier-lab-stop-its-swarming-agents/) - TechCrunch on the Decisions API at DevDay. Luna-based, limited preview, vision claimed. No public docs page yet, so this is the citation.
- [Amazon releases its own Jev clone](https://techcrunch.com/2026/10/01/amazon-releases-its-own-jev-clone-as-decision-models-flood-the-web/) - TechCrunch on Strands Decider 2B.
- [Cloudflare announcement](https://x.com/Cloudflare/status/2105747536510099540) - Birthday Week post for Clef. Swap for a docs URL when one exists.
- [Perplexity Decisions API](https://x.com/AravSrinivas/status/2105774153903268288) - Launch post for the hosted Decisions API.
- [Perplexity follow-up](https://x.com/AravSrinivas/status/2106119404433908149) - Follow-up on the decider versus Jev.

## Related

- [Awesome Claude Managed Agents](https://github.com/paulmeller/awesome-managed-agents) - Curated list for Anthropic’s managed agent runtime.
- [Awesome Agent Client Protocol](https://github.com/paulmeller/awesome-agent-client-protocol) - Curated list for ACP.

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.
