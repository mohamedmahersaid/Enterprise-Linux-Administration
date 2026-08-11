# Containers & Virtualization on Linux

Running workloads on Linux without a hypervisor vendor or an orchestrator: rootless containers, image supply chain, and KVM virtualisation. Assumes System Administration, storage and networking. Outcome: you can run containers as a non-root user with systemd integration, build and sign images you can account for, and operate KVM guests including migration and recovery. Excludes Kubernetes and OpenShift (Containers and Kubernetes, and Red Hat Ecosystem) and VMware. Completion evidence: a rootless service surviving reboot under systemd, a signed image with recorded provenance, and a live migration performed without guest downtime.

[Back to Linux](../../README.md)

## Branches

- [Rootless Containers & Image Supply Chain](lx-branch-podman/README.md) — 3 leaves
- [KVM Virtualization](lx-branch-kvm/README.md) — 3 leaves
