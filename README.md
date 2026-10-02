# Awesome Decisions API [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Models and APIs that *pick* — choice, score, or yes/no with a probability — instead of writing chat. TypeSafe Jev opened the category; OpenAI, Cloudflare, Perplexity, and others shipped peers in late September and early October 2026.

## Contents

- [Official Resources](#official-resources)
- [Models](#models)
- [SDKs and Clients](#sdks-and-clients)
- [Documentation](#documentation)
- [Tutorials and Guides](#tutorials-and-guides)
- [Community Projects](#community-projects)
- [Articles and Press](#articles-and-press)
- [Related](#related)

## Official Resources

- [Introducing System One and Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev) - TypeSafe announcement of the decision-model category and Jev.
- [Jev on Cloudflare Workers AI](https://developers.cloudflare.com/ai/models/typesafe/jev/) - Hosted `typesafe/jev` on Workers AI.
- [Clef and Clef-flash](https://blog.cloudflare.com/clef-decision-models/) - Cloudflare’s Jev-API-compatible decision models (vision, 64k context, Apache-2.0).
- [Cloudflare announcement](https://x.com/Cloudflare/status/2105747536510099540) - Birthday Week post for Clef.
- [Perplexity Decisions API](https://x.com/AravSrinivas/status/2105774153903268288) - Launch post for `pplx-decider-v1-27b` and the hosted Decisions API.
- [Perplexity follow-up](https://x.com/AravSrinivas/status/2106119404433908149) - Follow-up on the decider versus Jev.
- [pplx-decider-v1-27b model card](https://huggingface.co/perplexity-ai/pplx-decider-v1-27b) - Open weights and the 11-benchmark table Perplexity published.
- [OpenAI Decisions API (TechCrunch)](https://techcrunch.com/2026/09/30/openais-jev-clone-could-help-the-frontier-lab-stop-its-swarming-agents/) - DevDay coverage. Public schema and pricing were still thin at publication.

## Models

- [TypeSafe Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev) - Text-only Choice, Score, and Noul with calibrated probabilities. Generally available; about $0.042 per million input tokens. Also on Cloudflare as `typesafe/jev`.
- [Cloudflare Clef and Clef-flash](https://blog.cloudflare.com/clef-decision-models/) - Jev-API compatible, vision, 64k context, Apache-2.0 weights, Workers AI, and RL fine-tune.
- [Perplexity pplx-decider-v1-27b](https://huggingface.co/perplexity-ai/pplx-decider-v1-27b) - Multimodal open weights. Hosted Decisions API about $0.04 per million input tokens. Perplexity reports it ahead of Jev on their 11-benchmark panel.
- [OpenAI Decisions API](https://techcrunch.com/2026/09/30/openais-jev-clone-could-help-the-frontier-lab-stop-its-swarming-agents/) - Luna-based, limited preview. Vision claimed; public request schema and price not published as of this list.
- [Strands Decider 2B](https://strandsagents.com/blog/introducing-strands-decider/) - AWS Strands Labs open-source 2B decision model (Choice, Noul, Score). Weights on [Hugging Face](https://huggingface.co/StrandsAgents/strands-decider-2B-hobson-v19); code at [strands-labs/strands-decider](https://github.com/strands-labs/strands-decider).
- [Inception Mercury Decide](https://openrouter.ai/inception/mercury-decide:free) - System One-shaped decision model on OpenRouter (`inception/mercury-decide:free`). Text in; choice, score, or yes/no with a probability.
- [LiquidAI D1](https://openrouter.ai/liquid/d1) - Hosted System One-shaped decision model. OpenRouter lists about $0.04 per million input tokens and free output.
- [Kev](https://github.com/jaredpalmer/kev) - Open-weight Jev-compatible family (Apache-2.0) with a local `/v1/systemone` server. Announcement: [Introducing Kev](https://jaredpalmer.com/blog/introducing-kev).

## SDKs and Clients

<!-- Add SDKs, CLIs, and client libraries here -->

## Documentation

<!-- Add API reference and how-to docs here -->

## Tutorials and Guides

<!-- Add walkthroughs and how-tos here -->

## Community Projects

<!-- Add open-source tools, wrappers, and demos here -->

## Articles and Press

- [OpenAI’s Jev clone](https://techcrunch.com/2026/09/30/openais-jev-clone-could-help-the-frontier-lab-stop-its-swarming-agents/) - TechCrunch on the Decisions API at DevDay.
- [Amazon releases its own Jev clone](https://techcrunch.com/2026/10/01/amazon-releases-its-own-jev-clone-as-decision-models-flood-the-web/) - TechCrunch on Strands Decider 2B.

## Related

- [Awesome Claude Managed Agents](https://github.com/paulmeller/awesome-managed-agents) - Curated list for Anthropic’s managed agent runtime.
- [Awesome Agent Client Protocol](https://github.com/paulmeller/awesome-agent-client-protocol) - Curated list for ACP.

## Contributing

Contributions welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.
