# Storage & Filesystems in Depth

Linux storage past the basics: layered local storage, encryption at rest, and shared and network filesystems. Assumes System Administration (partitions, filesystems, mounts). Outcome: you can design a storage layout that survives a disk failure, an encrypted volume that unlocks without a human at the console, and a network filesystem that fails over without corrupting a client. Excludes Ceph and distributed object storage (Red Hat Ecosystem) and cloud block storage. Completion evidence: an LVM layout with a tested snapshot restore, an encrypted volume with automated unlock, and a documented recovery from a simulated disk loss.

[Back to Linux](../../README.md)

## Branches

- [Advanced Local Storage](lx-branch-advstorage/README.md) — 3 leaves
- [Network & Shared Storage](lx-branch-netstorage/README.md) — 3 leaves
