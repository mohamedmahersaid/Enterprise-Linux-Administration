# Linux Foundations

The layer that was missing beneath everything else. Before this tree existed, lx-tree-sysadmin was the root of the Linux forest and a learner could reach eBPF, Ceph or LVM without having been taught users, permissions, packages or routing - the forest measured 55 of 79 leaves at Advanced or above with three Beginner leaves in total. Purpose: establish the primitives every later tree assumes. Outcome: you can create and remove an account so that access genuinely ends, diagnose permission denied by identifying WHICH of four access-control layers is denying, and reason about ownership rather than reaching for chmod 777. Prerequisites: none - this is the entry point. Excludes advanced storage, kernel tuning and fleet operations, which have their own trees. Completion evidence: a working offboarding procedure tested against an account holding an SSH key, and a permission diagnosis that names the blocking layer.

[Back to Linux](../../README.md)

## Branches

- [Accounts and Access](lx-branch-accounts-access/README.md) — 4 leaves
- [Software and Processes](lx-branch-software-processes/README.md) — 4 leaves
