# Agent Room — PostgreSQL production patterns for the Debian book

Status: analysis/reference only; not an installed skill, implementation, or approved specification.

Source: [msitarzewski/agent-room](https://github.com/msitarzewski/agent-room). Revision and license: [source ledger](../SOURCES.md).

## Problem and observed source pattern

A real service can teach persistence and operations more effectively than an isolated sample table. [README.md](https://github.com/msitarzewski/agent-room/blob/c48e8036159c2bf0a03473a3352457a2ef2c3e7e/README.md) describes PostgreSQL-backed commands, immutable events, projections, outboxes, audit, and sessions. [deploy/README.md](https://github.com/msitarzewski/agent-room/blob/c48e8036159c2bf0a03473a3352457a2ef2c3e7e/deploy/README.md) documents PostgreSQL 18, pgBackRest, systemd confinement/credentials, loopback database access, forward migrations, coordinated artifact/database backups, and isolated restore drills.

Its production target is Ubuntu Linux/amd64, not a verified Debian deployment. The documented reverse proxy is Caddy.

## What to mine

Study [db/migrations/0001_foundation.sql](https://github.com/msitarzewski/agent-room/blob/c48e8036159c2bf0a03473a3352457a2ef2c3e7e/db/migrations/0001_foundation.sql), [deploy/backup.sh](https://github.com/msitarzewski/agent-room/blob/c48e8036159c2bf0a03473a3352457a2ef2c3e7e/deploy/backup.sh), and [deploy/restore.sh](https://github.com/msitarzewski/agent-room/blob/c48e8036159c2bf0a03473a3352457a2ef2c3e7e/deploy/restore.sh) next. Extract transaction boundaries, schema evolution, recoverable outboxes, health/readiness, and consistency between database metadata and artifact storage.

## Proposed Debian adaptation

Build an AI-optional book lab: application service, PostgreSQL, systemd, TLS proxy, structured logs, backup job, and firewall. Teach least-privilege roles, separate migration/runtime access, secret/file permissions, grants/revocation, backup/restore, and failure recovery. Candidate domain entities include projects, commands, events, artifacts, approvals, and audit records; this is a teaching proposal, not a literal upstream table inventory.

## Exclusions and next analysis

Do not run Ubuntu bootstrap scripts unchanged on Debian or assume application rollback reverses migrations. Validate Debian packages, PostgreSQL version, confinement, credentials, and proxy choices separately. Start with disposable database tests and prove restoration of both data and artifacts. Keep AI workers optional and isolated from the core administration lessons.
