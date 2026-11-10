# Distributed Systems

What changes when there is more than one machine, and the machines must agree.

Planned, in reading order:

- [ ] How systems fail (crash-stop, omission, Byzantine; the network and timing model and its fallacies; gray failures; overload and metastable failure)
- [ ] Time, clocks, and ordering (physical clocks lie; Lamport clocks, happens-before, vector clocks)
- [ ] The network: protocols and what they cost (TCP and TLS behavior, HTTP/2 and 3, DNS, load balancing, connection pooling, timeouts as a budget)
- [ ] Replication (single-leader, multi-leader, leaderless and quorums)
- [ ] Partitioning (consistent hashing, hot keys, rebalancing)
- [ ] Failure detection, membership, and gossip (heartbeats, phi-accrual, SWIM, anti-entropy)
- [ ] Consistency models (linearizability down to eventual; CAP treated honestly; PACELC)
- [ ] Transactions and isolation levels (snapshot isolation, write skew)
- [ ] Consensus (why it is provably hard: two generals, FLP; Raft intuition; fencing tokens)
- [ ] Delivery guarantees (at-most, at-least, exactly-once; the end-to-end argument as the organizing principle)
- [ ] Caching as a consistency problem (a cache is a replica with no protocol; TTL as eventual consistency; stampedes)
- [ ] Determinism, replay, and state machine replication (ordered log plus deterministic machine equals reproducible state; recorded nondeterminism; the theory under checkpoint/resume and reproducible evals)
