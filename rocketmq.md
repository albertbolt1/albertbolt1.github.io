## Open Source Contributions

### RocketMQ Rust (Apache-style Message Queue Implementation)

🔗 https://github.com/mxsm/rocketmq-rust

This project is a Rust-based reimplementation inspired by Apache RocketMQ. I contributed while using it as a way to learn Rust and deeply understand how large-scale distributed message queue systems (like those used at Alibaba scale) are architected.

The work also helped me explore distributed systems concepts such as replication, failover, and controller-based coordination.

---

### Key Contributions

<details>
<summary><b>CLI Enhancements for Controller Configuration</b></summary>

- Implemented CLI support to update controller configuration dynamically using key-value pairs
- Enabled runtime modification of controller cluster settings via command-line interface
- Worked with controller cluster configuration logic involving:
  - Cluster formation of controller nodes
  - dLedger-based Raft consensus for leader election
  - Failover coordination between master and replica nodes
- The controller selects a leader based on replication catch-up state and cluster health
- Understood and worked with distributed coordination mechanisms used for high availability

</details>

---

<details>
<summary><b>User Management CLI Command</b></summary>

- Added CLI command to update user information in the system
- Implemented backend logic to:
  - Parse CLI input into structured DTOs
  - Validate and process user update requests
  - Apply updates to broker-side user authorization data
- Users are used for:
  - Producer and consumer authorization
  - Access control for broker operations

</details>

---

<details>
<summary><b>Replica Information API</b></summary>

- Implemented backend functionality to fetch replica metadata for controllers
- Assisted in improving observability of replication state across nodes
- Helped understand replication consistency tracking in distributed systems

</details>

---

<details>
<summary><b>Time Zone Handling Utility</b></summary>

- Added a function to resolve local time based on IANA time zones provided via environment variables
- Introduced `LOG_TIMEZONE` configuration support (defaults to UTC)
- Ensures logs use correct and unambiguous timestamps using IANA time zone standards (e.g., `Asia/Kolkata`, `Europe/Berlin`)
- Avoids ambiguity of abbreviations like `IST`, which can represent multiple regions
- Ensures proper handling of Daylight Saving Time (DST)
- Replaced unsafe local offset detection with `OffsetTime` for safer and more predictable behavior

</details>

---

### Other Work

- Added unit tests to improve coverage and reliability
- Contributed documentation improvements
- Refactored existing code for clarity and maintainability

---

### What I learned

Working on this project gave me hands-on exposure to:

- Distributed systems design and controller-based coordination
- Raft-style consensus concepts (via dLedger)
- Message queue architecture at scale
- Rust language fundamentals and systems programming patterns
- Real-world trade-offs in replication and failover systems