# Networking & Core Services

The Linux network stack and the core services that ride on it: addressing and routing, packet filtering, name resolution, time and service availability. Assumes System Administration and Foundations networking. Outcome: you can trace a packet from application to wire, write a filtering policy you can justify rule by rule, and keep name resolution and time correct - the two dependencies that break everything else silently when wrong. Excludes advanced multi-homing and VRF design (Advanced Linux Networking) and cloud networking. Completion evidence: a documented packet path, a firewall policy with no rule nobody can explain, and a demonstrated recovery from DNS and clock failure.

[Back to Linux](../../README.md)

## Branches

- [Network Stack & Filtering](lx-branch-netstack/README.md) — 4 leaves
- [Service Availability & Time](lx-branch-svcavail/README.md) — 3 leaves
