# Linux catalog

Enterprise Linux administration: storage, boot, performance tuning, and security hardening on RHEL-family systems.

## Linux Foundations

The layer that was missing beneath everything else. Before this tree existed, lx-tree-sysadmin was the root of the Linux forest and a learner could reach eBPF, Ceph or LVM without having been taught users, permissions, packages or routing - the forest measured 55 of 79 leaves at Advanced or above with three Beginner leaves in total. Purpose: establish the primitives every later tree assumes. Outcome: you can create and remove an account so that access genuinely ends, diagnose permission denied by identifying WHICH of four access-control layers is denying, and reason about ownership rather than reaching for chmod 777. Prerequisites: none - this is the entry point. Excludes advanced storage, kernel tuning and fleet operations, which have their own trees. Completion evidence: a working offboarding procedure tested against an account holding an SSH key, and a permission diagnosis that names the blocking layer.

### Accounts and Access

- **Beginner:** [Local Users, Groups, Password Aging and Account Lifecycle on RHEL](docs/lx-tree-foundations/lx-branch-accounts-access/lx-foundations-users-groups.md)
- **Beginner:** [Linux File Permissions, umask and Special Permission Bits](docs/lx-tree-foundations/lx-branch-accounts-access/lx-foundations-permissions-umask.md)
- **Intermediate:** [Linux File Permissions Beyond Mode Bits: ACLs and File Capabilities](docs/lx-tree-foundations/lx-branch-accounts-access/lx-foundations-acls-capabilities.md)
- **Intermediate:** [Linux Privilege Delegation with sudo, sudoers and Least Privilege](docs/lx-tree-foundations/lx-branch-accounts-access/lx-foundations-sudo-delegation.md)

### Software and Processes

- **Beginner:** [RPM, DNF, Repositories and Package Verification](docs/lx-tree-foundations/lx-branch-software-processes/lx-foundations-rpm-dnf.md)
- **Beginner:** [cron, at and systemd Timers for Scheduled Work](docs/lx-tree-foundations/lx-branch-software-processes/lx-foundations-cron-timers.md)
- **Beginner:** [Shell Environment, PATH and Environment Variables](docs/lx-tree-foundations/lx-branch-software-processes/lx-foundations-shell-environment.md)
- **Beginner:** [Linux Processes Signals systemd Job Control and Process Troubleshooting](docs/lx-tree-foundations/lx-branch-software-processes/lx-processes-signals.md)

## System Administration

Core RHCSA/RHCE-level administration: LVM storage, filesystems, systemd, and boot management.

### Storage Management

- **Intermediate:** [LVM: Online Volume Extension](docs/lx-tree-sysadmin/lx-branch-storage/lx-lvm-extend.md)
- **Intermediate:** [Filesystems: XFS, ext4 and Persistent Mounts](docs/lx-tree-sysadmin/lx-branch-storage/lx-fs-mgmt.md)

### Systemd & Boot

- **Intermediate:** [Systemd Units and Custom Services](docs/lx-tree-sysadmin/lx-branch-systemd/lx-systemd-units.md)
- **Intermediate:** [Boot Process, Targets and Root Password Recovery](docs/lx-tree-sysadmin/lx-branch-systemd/lx-boot-targets.md)

## Performance & Security

Tuning RHEL for throughput and latency, and hardening it with SELinux and firewalld.

### Performance Tuning

- **Advanced:** [Tuned Profiles and Kernel Tuning with sysctl](docs/lx-tree-perfsec/lx-branch-perf/lx-tuned-sysctl.md)
- **Expert:** [Performance Analysis: USE Method and Core Tools](docs/lx-tree-perfsec/lx-branch-perf/lx-perf-analysis.md)

### SELinux & Firewalld

- **Advanced:** [SELinux: Contexts, Booleans and Troubleshooting](docs/lx-tree-perfsec/lx-branch-security/lx-selinux.md)
- **Intermediate:** [Firewalld: Zones, Services and Rich Rules](docs/lx-tree-perfsec/lx-branch-security/lx-firewalld.md)

## Performance, Networking & Automation at Scale

Enterprise-grade Linux networking with NetworkManager and bonding, live diagnostics, and fleet-scale provisioning and patch automation.

### Advanced Linux Networking

- **Advanced:** [NetworkManager: nmcli, Bonding, Teaming and VLANs](docs/lx-tree-netauto/lx-branch-netconfig/lx-nm-bonding.md)
- **Advanced:** [Linux Network Troubleshooting: tcpdump Packet Capture and Diagnostic Bundles](docs/lx-tree-netauto/lx-branch-netconfig/lx-net-troubleshoot.md)

### Fleet Automation & Provisioning

- **Advanced:** [Kickstart Automation and Image Builds](docs/lx-tree-netauto/lx-branch-fleetauto/lx-kickstart-imagebuilder.md)
- **Expert:** [Fleet Patch Automation with dnf and Ansible](docs/lx-tree-netauto/lx-branch-fleetauto/lx-fleet-patching.md)

## Storage & Filesystems in Depth

Linux storage past the basics: layered local storage, encryption at rest, and shared and network filesystems. Assumes System Administration (partitions, filesystems, mounts). Outcome: you can design a storage layout that survives a disk failure, an encrypted volume that unlocks without a human at the console, and a network filesystem that fails over without corrupting a client. Excludes Ceph and distributed object storage (Red Hat Ecosystem) and cloud block storage. Completion evidence: an LVM layout with a tested snapshot restore, an encrypted volume with automated unlock, and a documented recovery from a simulated disk loss.

### Advanced Local Storage

- **Intermediate:** [Software RAID with mdadm](docs/lx-tree-storage-adv/lx-branch-advstorage/lx-mdraid.md)
- **Advanced:** [Multipath, Fibre Channel and NVMe over Fabrics](docs/lx-tree-storage-adv/lx-branch-advstorage/lx-multipath.md)
- **Intermediate:** [Stratis, VDO and Modern Storage Efficiency](docs/lx-tree-storage-adv/lx-branch-advstorage/lx-stratis-vdo.md)

### Network & Shared Storage

- **Intermediate:** [NFS Server and Client at Enterprise Scale](docs/lx-tree-storage-adv/lx-branch-netstorage/lx-nfs.md)
- **Intermediate:** [Samba File Services and Active Directory Integration](docs/lx-tree-storage-adv/lx-branch-netstorage/lx-samba.md)
- **Intermediate:** [iSCSI Target and Initiator Configuration](docs/lx-tree-storage-adv/lx-branch-netstorage/lx-iscsi.md)

## Identity, Access & Compliance

Identity, authentication and compliance on Linux hosts: directory integration, authorisation policy, auditing and hardening benchmarks. Assumes System Administration and basic networking, DNS and time synchronisation. Outcome: you can join a host to a central directory, control who may do what with HBAC and sudo, and produce compliance evidence an auditor accepts. Excludes IdM SERVER operations, which belong to the Red Hat Ecosystem forest - this tree owns the CLIENT side (SSSD, authselect, enrolment). Completion evidence: an enrolled host authenticating against the directory, a scoped sudo policy, and a compliance scan with tailored exceptions justified.

### Identity & Authentication

- **Advanced:** [SSSD, Red Hat IdM and Active Directory Enrolment](docs/lx-tree-idcomp/lx-branch-identity/lx-sssd-idm.md)
- **Advanced:** [PAM Stack Design and sudo Policy](docs/lx-tree-idcomp/lx-branch-identity/lx-pam-sudo.md)
- **Intermediate:** [SSH Hardening and Certificate Authentication](docs/lx-tree-idcomp/lx-branch-identity/lx-ssh-hardening.md)

### Compliance & Auditing

- **Intermediate:** [OpenSCAP, CIS Benchmarks and STIG Remediation](docs/lx-tree-idcomp/lx-branch-compliance/lx-openscap.md)
- **Advanced:** [auditd Rules and Forensic Trails](docs/lx-tree-idcomp/lx-branch-compliance/lx-auditd.md)
- **Advanced:** [FIPS Mode and System-Wide Crypto Policies](docs/lx-tree-idcomp/lx-branch-compliance/lx-fips-crypto.md)

## Networking & Core Services

The Linux network stack and the core services that ride on it: addressing and routing, packet filtering, name resolution, time and service availability. Assumes System Administration and Foundations networking. Outcome: you can trace a packet from application to wire, write a filtering policy you can justify rule by rule, and keep name resolution and time correct - the two dependencies that break everything else silently when wrong. Excludes advanced multi-homing and VRF design (Advanced Linux Networking) and cloud networking. Completion evidence: a documented packet path, a firewall policy with no rule nobody can explain, and a demonstrated recovery from DNS and clock failure.

### Network Stack & Filtering

- **Advanced:** [nftables and firewalld Rule Design](docs/lx-tree-netsvc/lx-branch-netstack/lx-nftables.md)
- **Intermediate:** [Bonding, Teaming, VLANs and Bridges](docs/lx-tree-netsvc/lx-branch-netstack/lx-bonding-vlan.md)
- **Advanced:** [DNS Server Design with BIND: Split-Horizon Zones and DNSSEC](docs/lx-tree-netsvc/lx-branch-netstack/lx-dns-bind.md)
- **Advanced:** [Linux Bridges veth Pairs and Network Namespace Virtual Networking](docs/lx-tree-netsvc/lx-branch-netstack/lx-bridges-netns.md)

### Service Availability & Time

- **Advanced:** [HAProxy and Keepalived High Availability](docs/lx-tree-netsvc/lx-branch-svcavail/lx-haproxy-keepalived.md)
- **Intermediate:** [Time Synchronisation with chrony and PTP](docs/lx-tree-netsvc/lx-branch-svcavail/lx-chrony-ptp.md)
- **Advanced:** [Pacemaker Clustering, Fencing and Quorum](docs/lx-tree-netsvc/lx-branch-svcavail/lx-pacemaker.md)

## Kernel, Performance & Observability

Kernel behaviour, resource control and observability: memory and cgroup limits, tracing, and boot and crash analysis. Assumes Performance and Security, plus comfort reading system metrics. Outcome: you can bound what a workload may consume, observe what it is actually doing rather than what it claims, and analyse a system that has already failed. Excludes application profiling and APM, and cloud-provider monitoring. Completion evidence: a cgroup policy that contains a runaway process, a trace that identifies a real bottleneck, and a crash dump analysed to a root cause.

### Resource Control & Memory

- **Advanced:** [cgroups v2 Resource Control and systemd Slices](docs/lx-tree-kernelperf/lx-branch-resource/lx-cgroups-v2.md)
- **Advanced:** [Linux Memory Analysis: Swap, Page Cache and the OOM Killer](docs/lx-tree-kernelperf/lx-branch-resource/lx-oom-memory.md)
- **Advanced:** [NUMA Topology, IRQ Affinity and Kernel Tuning](docs/lx-tree-kernelperf/lx-branch-resource/lx-numa-tuning.md)

### Tracing & Boot Analysis

- **Advanced:** [eBPF and bpftrace Production Tracing](docs/lx-tree-kernelperf/lx-branch-observe/lx-ebpf-bpftrace.md)
- **Intermediate:** [Boot Performance Analysis with systemd-analyze](docs/lx-tree-kernelperf/lx-branch-observe/lx-boot-analysis.md)
- **Advanced:** [Block IO Schedulers, Queue Depth and Storage Latency](docs/lx-tree-kernelperf/lx-branch-observe/lx-io-tuning.md)

## Containers & Virtualization on Linux

Running workloads on Linux without a hypervisor vendor or an orchestrator: rootless containers, image supply chain, and KVM virtualisation. Assumes System Administration, storage and networking. Outcome: you can run containers as a non-root user with systemd integration, build and sign images you can account for, and operate KVM guests including migration and recovery. Excludes Kubernetes and OpenShift (Containers and Kubernetes, and Red Hat Ecosystem) and VMware. Completion evidence: a rootless service surviving reboot under systemd, a signed image with recorded provenance, and a live migration performed without guest downtime.

### Rootless Containers & Image Supply Chain

- **Advanced:** [Podman Rootless Containers and systemd Integration](docs/lx-tree-containervirt/lx-branch-podman/lx-podman-rootless.md)
- **Intermediate:** [Image Building with Buildah and Registry Operations with Skopeo](docs/lx-tree-containervirt/lx-branch-podman/lx-buildah-skopeo.md)
- **Advanced:** [Container Storage Drivers, Layers and SELinux Labelling](docs/lx-tree-containervirt/lx-branch-podman/lx-container-storage.md)

### KVM Virtualization

- **Advanced:** [KVM and libvirt Performance Tuning](docs/lx-tree-containervirt/lx-branch-kvm/lx-kvm-libvirt.md)
- **Intermediate:** [Golden Images with Image Builder and Kickstart](docs/lx-tree-containervirt/lx-branch-kvm/lx-image-builder.md)
- **Advanced:** [VM Conversion and Migration with virt-v2v](docs/lx-tree-containervirt/lx-branch-kvm/lx-vm-migration.md)

## Enterprise Operations at Fleet Scale

Operating many Linux hosts rather than one: content and patch lifecycle, centralised logging, and fleet administration. Assumes Advanced Networking and Automation, plus configuration delivery. Outcome: you can stage a patch across an estate with a rollback path, centralise logs so an outage does not destroy its own evidence, and administer hosts at scale without manual drift. Excludes Satellite PRODUCT operations and AAP, which belong to the Red Hat Ecosystem forest - this tree owns vendor-neutral fleet practice. Completion evidence: a staged patch wave with measured exposure windows, a log pipeline that buffers through an outage, and a drift report against a declared baseline.

### Content, Patching & Lifecycle

- **Advanced:** [Red Hat Satellite: Content Views and Lifecycle Environments](docs/lx-tree-fleetops/lx-branch-patching/lx-satellite.md)
- **Intermediate:** [DNF and YUM Package Management: Modules, Repository Priority and Version Locking](docs/lx-tree-fleetops/lx-branch-patching/lx-dnf-modules.md)
- **Advanced:** [Live Kernel Patching and Reboot Orchestration](docs/lx-tree-fleetops/lx-branch-patching/lx-kpatch-reboot.md)

### Logging & Fleet Management

- **Intermediate:** [journald, rsyslog and Central Log Aggregation](docs/lx-tree-fleetops/lx-branch-obslog/lx-journald-rsyslog.md)
- **Beginner:** [Cockpit and Ansible Web-Based Linux Fleet Administration](docs/lx-tree-fleetops/lx-branch-obslog/lx-cockpit.md)
- **Advanced:** [Ansible Configuration Baselines and Drift Remediation](docs/lx-tree-fleetops/lx-branch-obslog/lx-ansible-baselines.md)

## Working Without Help: Documentation, Rescue and Diagnosis

Three capabilities that only matter when the usual routes are closed - no search engine, no colleague, no running system. Reading the documentation that ships with the machine, recovering one that will not boot, and finding out what is holding a resource open.

### Self-Service Documentation, Boot Recovery and Descriptor Diagnostics

- **Beginner:** [Linux Man Pages Bash Help and systemd Documentation for Self-Service Troubleshooting](docs/lx-tree-self-reliance/lx-branch-selfservice-recovery/lx-man-pages-docs.md)
- **Advanced:** [Linux Rescue Mode Emergency Boot Recovery and initramfs Repair](docs/lx-tree-self-reliance/lx-branch-selfservice-recovery/lx-rescue-boot-recovery.md)
- **Advanced:** [Linux lsof Open File Descriptors ulimit and systemd Resource Limit Troubleshooting](docs/lx-tree-self-reliance/lx-branch-selfservice-recovery/lx-lsof-file-descriptors.md)

## Linux Estate Operations: Primitives, Diagnosis and Lifecycle

Twelve concerns that a Linux estate runs on and that the forest had no leaf for: what a process and a bridge actually are, how access is constrained and integrity verified, how workloads are hosted, how a failure is diagnosed rather than guessed at, and how the estate is patched, upgraded and paid for.

### Mandatory Access Control and File Integrity

- **Advanced:** [AppArmor Profiles SELinux Comparison and Mandatory Access Control Hardening on Linux](docs/lx-tree-estate-operations/lx-branch-mac-integrity/lx-apparmor-mac.md)
- **Advanced:** [AIDE File Integrity Monitoring and Baseline Verification on Linux](docs/lx-tree-estate-operations/lx-branch-mac-integrity/lx-aide-fim.md)

### Hosting Workloads on Linux

- **Advanced:** [LXC System Containers and Linux Container Isolation Without Docker](docs/lx-tree-estate-operations/lx-branch-hosting-workloads/lx-lxc-containers.md)
- **Intermediate:** [nginx and Apache Web Server Configuration and Reverse Proxy on Linux](docs/lx-tree-estate-operations/lx-branch-hosting-workloads/lx-web-servers.md)
- **Advanced:** [Postfix SMTP Relay systemd Service and Linux Mail Delivery Troubleshooting](docs/lx-tree-estate-operations/lx-branch-hosting-workloads/lx-postfix-relay.md)

### Crash Analysis and Diagnostic Method

- **Advanced:** [Linux Core Dumps systemd coredumpctl and Application Crash Troubleshooting](docs/lx-tree-estate-operations/lx-branch-diagnosis/lx-core-dumps.md)
- **Advanced:** [Systematic Linux Diagnostic Methodology and Performance Troubleshooting Order](docs/lx-tree-estate-operations/lx-branch-diagnosis/lx-diagnostic-method.md)

### Patching, Lifecycle and Commercial Models

- **Advanced:** [Linux Patch Management yum dnf apt Repository and Errata Strategy](docs/lx-tree-estate-operations/lx-branch-lifecycle-commercial/lx-patch-repos.md)
- **Advanced:** [Linux OS Lifecycle End-of-Life Planning and Major Version Upgrade Paths](docs/lx-tree-estate-operations/lx-branch-lifecycle-commercial/lx-os-lifecycle.md)
- **Advanced:** [RHEL Ubuntu Pro and SLES Subscription Licensing and Enterprise Support Models](docs/lx-tree-estate-operations/lx-branch-lifecycle-commercial/lx-linux-licensing.md)

## Script Safety, Fleet Drift, Snapshots and Resource Accounting

Four host-level disciplines: writing an administrative script that cannot destroy a production system, understanding what actually drifts between configuration runs, knowing why a filesystem snapshot is not a backup, and reading per-service consumption from the accounting the kernel already keeps.

### Script Safety and Fleet Drift

- **Intermediate:** [Bash Scripting for Linux System Administration Error Handling and Safety](docs/lx-tree-fleet-discipline/lx-branch-script-fleet/lx-bash-admin.md)
- **Advanced:** [Linux Fleet Management at Scale with Ansible and systemd Configuration Drift](docs/lx-tree-fleet-discipline/lx-branch-script-fleet/lx-fleet-management.md)

### Snapshots and Resource Accounting

- **Advanced:** [Linux Backup Strategy Filesystem Snapshots and Restore Verification](docs/lx-tree-fleet-discipline/lx-branch-snapshots-capacity/lx-backup-strategy.md)
- **Advanced:** [Linux Fleet Capacity Planning Rightsizing and systemd Resource Accounting](docs/lx-tree-fleet-discipline/lx-branch-snapshots-capacity/lx-capacity-planning.md)
