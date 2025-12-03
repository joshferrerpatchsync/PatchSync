# PatchSync

Multi-agent code generation for complex repositories.

## The Problem

Current AI code generation tools edit files sequentially. On complex repositories with interdependent code—monorepos, cascading logic, shared state—this breaks:

- Rename a type in File A, imports in File B become stale
- Modify a state machine, forget to update all handlers
- Change validation in one place, break it in five others

You're left with broken imports, inconsistent state, and hours of manual fixing.

## The Solution

PatchSync uses a coordinated multi-agent approach:

1. **Understand the full scope** — All agents understand what changes are happening across all files
2. **Generate in parallel** — Multiple agents generate patches simultaneously instead of sequentially
3. **Merge intelligently** — Detect cross-file issues *before* applying anything
4. **Never break** — Deterministic coordination ensures consistency

Result: All files edited together, coordinated, no conflicts.

## Key Capabilities

- **Parallel code generation** — Edit 10 files in the time Cursor edits 1
- **Complex repo support** — Handles monorepos, circular dependencies, cascading logic
- **Deterministic coordination** — No probabilistic conflicts; issues are caught at generation time
- **Multi-stage review** — Planner → Coder(s) → Reviewer → Final Reviewer → Director
- **Intelligent risk assessment** — High-risk changes get extra scrutiny; low-risk changes move fast
- **Learning & retries** — System learns from failures and tries again with updated constraints

## Status

🚧 **In Development**

**Target:** VS Code extension prototype in Q1 2026

## Getting Started

This is an early-stage project. The codebase is under active development.

## Architecture Philosophy

PatchSync is built on three core principles:

1. **Determinism** — Given identical inputs, the system produces identical results. No probabilistic failures.
2. **Coordination** — Multi-agent work is explicitly coordinated, not hoped to work out.
3. **Safety** — No uncontrolled writes; all mutations are validated before application.

The system is designed for repos where sequential editing fails—not as a faster version of existing tools, but as a fundamentally different approach to the problem.

## Contact

Interested in early access or partnership?

📧 josh@patchsync.dev  
🌐 [patchsync.dev](https://patchsync.dev)

---

**PatchSync** — Building the code generation system for the repos that sequential tools can't touch.
