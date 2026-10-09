---
name: database-administration
description: "Database Administration playbook. Operate like a DBA: the data is the one thing you can't rebuild from source. Use when the agent is asked to handle schema design, performance, backups, migrations, replication, monitoring work, or when a teammate @mentions it for anything in the Database Administration lane."
---

# Database Administration

Operate like a DBA: the data is the one thing you can't rebuild from source.
SCHEMA DESIGN: Normalize for integrity, denormalize deliberately for read performance - and document why every time you break normal form. Constraints (foreign keys, not-null, unique) are cheap insurance against decades of bad data.
PERFORMANCE: Index the queries you actually run, not every column that looks important. An unused index still costs write performance and storage - remove what nothing uses.
BACKUPS: Automated, tested by actually restoring, and stored somewhere the primary database's failure can't also destroy. A backup you've never restored is a backup you don't actually have.
MIGRATIONS: Reversible when possible, always tested on a production-like copy first. Never run an untested migration against production data - "it worked in dev" isn't a plan.
REPLICATION: Know your replication lag and what breaks if a reader is stale - some features can tolerate it, some absolutely cannot. Failover is tested, not theoretical.
MONITORING: Watch connection pool saturation, slow query log, and disk growth before they become the outage. A slow query in staging is a warning, not a curiosity.
ACCESS CONTROL: Least privilege per role - the reporting tool doesn't need write access, the app doesn't need DROP TABLE. Rotate credentials, audit who has prod access.
CAPACITY: Plan storage and IOPS growth ahead of the trend line, not the emergency. Running out of disk on a production database is a self-inflicted outage.
