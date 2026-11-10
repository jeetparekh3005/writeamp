# Foundations

The theory the rest of the notebook stands on. Organized by concept; DDIA and other
books index *into* here from [`../reading`](../reading).

## The spine

Three pages everything else references:

1. **The log** (in [`data-systems/`](./data-systems)) - the single abstraction under half of computing: the WAL, LSM memtables, replication streams, Kafka, event sourcing, undo logs, and an agent's context.
2. **How systems fail** (in [`distributed-systems/`](./distributed-systems)) - crash-stop, omission, Byzantine; the network and timing model (slow is indistinguishable from dead); gray failures; overload and metastable failure.
3. **Time, clocks, and ordering** (in [`distributed-systems/`](./distributed-systems)) - physical clocks lie; Lamport clocks, happens-before, vector clocks.

## The sections

- [`data-systems/`](./data-systems) - the log, storage engines, streams and batch, durability and disaster recovery, encoding and live migration, indexing. *(DDIA Ch 1-4, 10-11)*
- [`distributed-systems/`](./distributed-systems) - failure, time, the network, replication, partitioning, membership, consistency, transactions, consensus, delivery guarantees, caching, determinism and replay. *(DDIA Ch 5-9, and beyond)*
- [`adversarial-systems/`](./adversarial-systems) - the same problems when components can lie: Byzantine fault tolerance, trust boundaries and verification, and the bridge from Byzantine quorums to agent reliability.

The through-line worth tracking: **consensus is consensus.** Raft in etcd and a BFT
quorum in an adversarial network solve the same problem under different fault models.
Cross-link accordingly.

## What this section deliberately does not cover

Infrastructure and platform specifics (Kubernetes, infrastructure-as-code, cloud vendor
primitives) age in dog years; this notebook aims at the theory that does not. Operational
practice (SLOs, observability, security engineering) lives in
[`../cross-cutting`](../cross-cutting); data structures and algorithm implementations live
in [`../algorithms`](../algorithms); integration styles and API design live in
[`../patterns/architectural`](../patterns/architectural). If a topic is missing from
foundations, it is either one of those, or it is an omission worth an issue.
