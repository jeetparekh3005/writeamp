# Data Systems

How data is stored, moved, evolved, and recovered. The log opens this section because
everything else in it is a view over a log.

Planned, in reading order:

- [ ] The log: the abstraction under half of computing (WAL, LSM, replication streams, event sourcing, agent context)
- [ ] Storage engines: why LSM and B-trees exist (write amplification, compaction, the read/write trade; mechanics live in [`../../algorithms`](../../algorithms))
- [ ] Streams and batch: the log in motion (event time vs processing time, watermarks, windows, stream-table duality, consistent snapshots)
- [ ] Durability and disaster recovery (what a write actually promises: fsync and group commit; replication is not backup; point-in-time recovery; RPO/RTO as a contract; an untested restore is not a backup)
- [ ] Encoding, schema evolution, and live migration (wire compatibility; expand-contract, the dual-write hazard, CDC as the safe cutover)
- [ ] Indexing and its costs (what an index buys and what it charges; vector indexes as just another index; sidebar: choosing a data model)
