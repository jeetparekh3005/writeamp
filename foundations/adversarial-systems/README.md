# Adversarial and Byzantine Systems

The same distributed problems, when components can lie. A crashed node is silent; a
Byzantine node answers on time, well-formed, and wrong. This section is the theory
behind the notebook's central bet: that this discipline is what AI systems in
production are missing.

Planned, in reading order:

- [ ] Trust boundaries and verification (signatures, Merkle structures, world state; then oracles, invariants, and golden sets: what counts as a verifier)
- [ ] From Byzantine quorums to agent reliability (the bridge page: a lean 3f plus 1 prelude; why voting needs independent failures; what breaks when membership is open and identities are free)

Cryptographic and data-structure building blocks (hashes, signatures, Merkle trees) live
in [`../../algorithms`](../../algorithms); this section covers why and where they hold a
system together, not how they are built.
