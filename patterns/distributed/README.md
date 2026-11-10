# Distributed Patterns

Coordination under failure: the recipes that keep distributed systems correct.

## The series: the transfer list, expanded

The launch article, [Your agent pipeline is a distributed system](../../ai-systems/agents/agent-pipelines-are-distributed-systems.md), makes seven claims and keeps each one to a paragraph. Each page in this series takes one claim and goes to the bottom of it: the mechanism, the failure modes, a diagram, and a verdict on what to steal and what to avoid.

Every page tells its story through the same system, so the architecture grows as the series does.

## Meet Gotham Savings & Loan

The bank's full architecture and incident history live on the [canon page](./gotham-savings-and-loan.md).

Gotham Savings & Loan is a fictional bank in a city you already know is fictional. Every incident in these pages is a composite. The problems are real.

Gotham S&L runs retail, commercial, and wealth lines on a mix any bank engineer will recognize:

- **The ledger**: the core banking system. The one source of truth, and the one system nobody is allowed to break.
- **The payments gateway**: cards, transfers, standing orders. Talks to external networks that answer late, twice, or not at all.
- **Onboarding and origination**: account opening and loan origination. Workflows that run for days and touch a dozen systems, some of them other companies'.
- **Statements and archival**: the read path for seven years of history, and the compaction story.
- **The agent desk**: the new initiative. LLM agents assisting operations, onboarding, and reconciliation. The reason the old discipline suddenly matters to a new audience.

One rule holds everywhere at Gotham S&L: money moves exactly once, or someone has a very bad week.

## Reading order

- [ ] Idempotency keys: the same payment, submitted twice
- [ ] The outbox: intent and effect are two different writes
- [ ] Admission control and backpressure: salary day
- [ ] Log compaction: seven years of statements
- [ ] Checkpoint and restore: the loan application that survived the deploy
- [ ] Sagas: unwinding a three-leg transfer
- [ ] Redundancy and verification: when reconciliation disagrees with the model

Each page is a living document; it gets rewritten as understanding improves. The dated, immutable versions of these ideas live in the articles.

Also planned, outside the series:

- [ ] Leader election
- [ ] Quorum
- [ ] Circuit breaker
- [ ] Bulkhead
- [ ] Retry with backoff + jitter
- [ ] Two-phase commit
