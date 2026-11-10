<img src="assets/brand/writeamp-wordmark.svg" alt="WriteAmp" width="540">

*Write once, read many.*

[![Deploy docs](https://github.com/jeetparekh3005/writeamp/actions/workflows/deploy-docs.yml/badge.svg)](https://github.com/jeetparekh3005/writeamp/actions/workflows/deploy-docs.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)

Read it as a site: <https://writeamp.com/>

WriteAmp is the working notebook of a technical architect, written after more than a
decade of building, scaling, and optimizing distributed systems. The core of it is a
single idea: the discipline we built for distributed systems over the last twenty years
(idempotency, backpressure, failure taxonomies, consensus) applies directly to the AI
systems everyone is now rushing into production, and almost nobody is applying it.

This is for senior engineers and architects, and the people on their way there. The
writing assumes you have shipped things and watched them fail.

It spans the full altitude of architectural thinking, from code-level patterns to
distributed and adversarial systems, alongside the practice of it: a system-design
methodology, real-world case studies (each ending in *what to steal, what to avoid*),
cross-cutting concerns, and a decision log. It grows with whatever I'm building.

## Map

| Area | What lives here |
|------|-----------------|
| [Foundations](./foundations) | Theory: [data systems](./foundations/data-systems), [distributed systems](./foundations/distributed-systems), [adversarial & Byzantine systems](./foundations/adversarial-systems) (BFT, trust boundaries, verification) |
| [Patterns](./patterns) | Three altitudes: [code](./patterns/code) (GoF), [architectural](./patterns/architectural) (CQRS, saga, hexagonal), [distributed](./patterns/distributed) (outbox, idempotency) |
| [Algorithms](./algorithms) | The toolbox: consistent hashing, bloom filters, HyperLogLog, CRDTs, merkle trees, consensus |
| [System Design](./system-design) | The method: estimation, component catalog, how to approach any design |
| [AI Systems](./ai-systems) | RAG, agents, extraction, agentic data, rules, LLMOps, AI architectures |
| [Case Studies](./case-studies) | Architecture teardowns of real systems, each ending in *steal / avoid* |
| [Cross-Cutting](./cross-cutting) | Reliability, observability, security, performance, cost |
| [Decisions](./decisions) | ADR log and *X vs Y, when and why* trade-off frameworks |
| [Engineering Leadership](./engineering-leadership) | Conway's law, team topologies, migration playbooks |
| [Reading](./reading) | Companions that index into the topic folders (e.g. [DDIA](./reading/ddia.md)) |

## How to read this notebook

- **Came from an article?** Start at the notebook page it links, then follow the ladder down.
- **Shipping AI to production?** Start at [AI Systems](./ai-systems) and follow the evals and verification thread into [Foundations](./foundations).
- **Studying for depth?** Start at the foundations spine: the log, how systems fail, time.
- **Designing something now?** Start at [System Design](./system-design) and follow the component and decision links.

## How it's organized

The notebook separates three kinds of thing, and `system-design/` is the method that
ties them together:

- **Knowledge** that teaches the primitives: `foundations/`, `patterns/`, `algorithms/`, `ai-systems/`
- **Judgment** you apply when designing: `decisions/`, `cross-cutting/`
- **Evidence** of the primitives composed in the wild: `case-studies/`

Topics are organized by concept, not by source. Books live in [`reading/`](./reading) as
indexes that link into the topic folders, so every concept has exactly one home.

## Conventions

- One concept per file, one home per concept; every other mention links to the home.
- Every page opens by placing itself on the altitude ladder: article (story) > pattern (recipe) > foundation (theory) > algorithm (structure).
- Living pages carry a "last compacted" date; articles are dated and never retroactively edited.
- Every case study ends with a **Steal / Avoid** section ([template](./case-studies/_template.md)).
- Every non-trivial choice gets an ADR in [`decisions/`](./decisions) ([template](./decisions/_template.md)).
- Diagrams are generated, not hand-drawn (see below), and referenced, not inlined.

## Diagrams

Architecture diagrams use the house engine in [`tools/diagram-forge/`](./tools/diagram-forge):
write a small JSON spec, get an animated diagram in one locked style (Neo-brutal on graph
paper; pulse = a call, dashed = async, thick = hot path). It exports a static SVG for
GitHub and the MkDocs site. The `/diagram-forge` skill turns a plain-language description
of a system into a spec and builds it.

## Roadmap

Depth over breadth, one node at a time. The primary workstream is the transfer-list
series in [`patterns/distributed/`](./patterns/distributed): each installment ships an
article, a pattern page, and a Gotham S&L incident. Foundations, algorithms, and
decisions pages are written when an installment needs to link to them, spine first.
Case studies follow the log thread: Cassandra, then Kafka, then the AI group.

---

Run the site locally with `pip install -r requirements-docs.txt && mkdocs serve`; pushes
to `main` auto-deploy via [GitHub Actions](./.github/workflows/deploy-docs.yml).
Contributions welcome ([CONTRIBUTING](./CONTRIBUTING.md)) under the [MIT](./LICENSE) license.
