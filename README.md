# Game Server Performance

Technical portfolio repository focused on **performance optimization for game servers and related systems**  
(Canary, OTClient, and Open Tibia ecosystem).

This project **does not expose source code**. Its purpose is to document real-world performance problems, technical approaches, and results achieved in **production environments**.

The actual code, patches, and tooling are maintained in **private repositories** and delivered through **assisted installation, tuning, and technical support**.

---

## Scope of Work

Work focused on **lag reduction**, **stability under load**, and **optimization of systems that handle large volumes of data, items, and updates**.

This portfolio covers optimizations across different layers of game servers and clients.

---

## Optimized Areas

### Item-heavy systems
- Item caching and access paths
- Stash, depot, and inbox
- Market (mass operations)
- Bulk NPC buy/sell actions
- Reduction of update storms caused by large item operations

### Persistence and saving
- Player save logic (with emphasis on inbox and large containers)
- House saving
- Database read/write optimization
- Reduction of redundant persistence operations
- Safer and more predictable save behavior under load

### Game loop and internal logic
- Zone system
- Item decay system
- Imbuements
- Forgeable / fiendish monster selection logic
- Cost reduction in critical loops and hot paths

### Infrastructure and server core
- Shared pointer usage and lifetime optimization
- Batching of server update packets
- CPU spike reduction during mass actions
- Server ↔ database communication optimization
- General stability improvements under peak load

---

## Observable Results

All work is validated using **real production metrics**, prioritizing **stability and predictability**, not just average performance.

Typical observed results include:
- Significant reduction of **CPU spikes** during peak hours
- Consistent drop in **p95/p99 latency** for item-heavy actions
- More stable player saves even with large data volumes
- Elimination of freezes caused by bulk operations
- Lower impact on the game loop during market, stash, and depot usage

> Absolute values vary depending on hardware, database, and configuration.  
> Improvements are evaluated through **before/after comparisons under equivalent scenarios**.

---

## Methodology

- Production bottleneck analysis
- Profiling focused on hot paths
- Realistic load testing
- Incremental and reversible optimizations
- Metrics-based validation (CPU, latency, tick time, database)
- No changes applied without a rollback strategy

---

## Delivery Model

This portfolio represents work delivered through:

- Application of private patch sets
- Assisted installation and integration
- Environment-specific tuning
- Ongoing technical support and maintenance
- Performance audits

**The code is not sold as a standalone product.**  
Delivery is provided as a **technical service**, ensuring compatibility, stability, and long-term support.

---

## Compatibility

- Game servers: Canary and related Open Tibia distributions
- Clients: OTClient and derivatives
- Database: MySQL / MariaDB
- Linux environments

Final compatibility depends on the specific version and infrastructure in use.

---

## Contact

For installation, performance audits, or technical support:

- GitHub Issues (initial contact)
- Discord / Telegram (upon request)

---

## Final Notes

This repository exists to **demonstrate technical capability and production experience**, not to distribute source code.

The focus is on solving **real performance problems** in game servers and clients operating under heavy load.
