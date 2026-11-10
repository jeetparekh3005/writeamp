# Case Studies

Architecture teardowns of real systems - where theory meets reality. Every study follows
the [template](./_template.md) and ends with a **Steal / Avoid** section; that footer is
the line between a teardown and an architect's note.

Sequenced by what each study feeds:

1. [`databases/`](./databases) - Cassandra first (feeds the log thread), then Spanner, DynamoDB, CockroachDB
2. [`streaming/`](./streaming) - Kafka next (feeds the log thread), then Flink, Pulsar
3. [`ai/`](./ai) - Harvey first (a regulated-industry AI teardown), then Perplexity, Cursor, Copilot
4. [`adversarial/`](./adversarial) - Byzantine systems at production scale; deferred until the adversarial foundations pages exist
5. [`products/`](./products) - Uber, Slack, Telegram, Netflix, Discord, Stripe; deferred

Each study links back into the primitives it uses (for example
[consistent hashing](../algorithms/consistent-hashing.md)) so the notebook reads as one
connected graph.
