# IT Support Lab

A home lab where I practise and document core IT support tasks: user and account management, endpoint patching, virtualisation, file permissions and basic networking.

Built by **Lesther Ndlovu** alongside my studies: IIE Higher Certificate in Information Technology in Support Services (NQF 5, distinction, 2025) and the IIE Bachelor of IT in Business Systems (part time, in progress).

> This is a small lab environment, not a production network. Each section says what I did, how, and what I learned.

## Lab environment

- Host machine: [e.g. Windows 11 laptop, 16 GB RAM]
- Hypervisor: Hyper-V (Generation 2 virtual machines)
- Virtual machines: [list them, e.g. Windows Server 2022 domain controller, 2 Windows 11 clients]
- Other tools: Action1 (remote monitoring and management), Cisco Packet Tracer

## Labs

| Lab | What I practised | Tools |
|---|---|---|
| [1. Active Directory](#1-active-directory) | User onboarding, bulk account creation, Group Policy, password resets | Active Directory, Group Policy |
| [2. Endpoint management](#2-endpoint-management-action1) | Remote diagnostics, software audits, patching | Action1 |
| [3. Virtual machines and recovery](#3-virtual-machines-and-recovery) | Building VMs, restoring a system | Hyper-V (Gen 2), System Restore |
| [4. File sharing and permissions](#4-file-sharing-and-permissions) | Sharing folders and controlling access | Windows file sharing, NTFS permissions |
| [5. Networking](#5-networking-cisco-packet-tracer) | VLANs, default gateways, interface status | Cisco Packet Tracer |

---

## 1. Active Directory

**Goal:** Manage users centrally the way a helpdesk or sysadmin would.

**What I did**
- Onboarded new users: [number] accounts created in [OU names]
- Bulk-provisioned accounts using [method, e.g. PowerShell script / CSV import]
- Configured Group Policy to [e.g. enforce a password policy / map a drive / restrict a setting]
- Reset user passwords and handled [e.g. account unlocks]

**Evidence:** screenshots are in the [`labimages`](labimages/) folder.

**What I learned:** Managing users centrally is faster and more consistent than touching each machine. Bulk provisioning saves time but also multiplies any mistake, so it pays to test a few accounts before rolling out. Group Policy applies by OU, so where an account sits decides which rules it gets.

---

## 2. Endpoint management (Action1)

**Goal:** Support and maintain machines remotely.

**What I did**
- Ran remote diagnostics on [number] machines
- Audited installed software
- Deployed patches: [e.g. which updates, how I confirmed they installed]

**Evidence:** screenshots are in the [`labimages`](labimages/) folder.

**What I learned:** Patching starts with knowing what is on each machine. A software audit shows what is installed and out of date, and it is not enough to push an update: I confirm afterwards that it actually installed.

---

## 3. Virtual machines and recovery

**Goal:** Build safe test environments and practise recovery.

**What I did**
- Created Generation 2 Hyper-V virtual machines
- Configured and tested System Restore: [e.g. made a restore point, broke something, restored it]

**Evidence:** screenshots are in the [`labimages`](labimages/) folder.

**What I learned:** Virtual machines let me break things safely and start again. System Restore only helps if a restore point exists before the problem, so recovery has to be set up before it is needed. Generation 2 VMs use UEFI, which affects which operating systems and images will boot.

---

## 4. File sharing and permissions

**Goal:** Give the right people access to the right files.

**What I did**
- Shared [folder] and set permissions for [groups or users]
- Tested access from a client machine: [what worked and what was blocked]

**Evidence:** screenshots are in the [`labimages`](labimages/) folder.

**What I learned:** Share permissions and NTFS permissions both apply, and the stricter one wins. I learned to test access from a client machine instead of assuming the settings work.

---

## 5. Networking (Cisco Packet Tracer)

**Goal:** Understand how a small LAN is segmented and troubleshot.

**What I did**
- Configured VLANs: [VLAN IDs and names]
- Set default gateways and checked connectivity between [devices]
- Checked interface status and fixed [e.g. a down interface]

**Evidence:** screenshots are in the [`labimages`](labimages/) folder.

**What I learned:** VLANs separate broadcast domains, but devices in different VLANs need a correct default gateway to communicate. When connectivity fails, I check interface status and the gateway first, because a down interface or wrong gateway is a common cause.

---

## Next on my list

- [e.g. CompTIA A+ or Microsoft AZ-900]
- [e.g. Microsoft Entra ID and Intune]
- [e.g. a ticketing tool such as Jira Service Management]

## Contact

Lesther Ndlovu, Braamfontein, Johannesburg · [email] · [LinkedIn, if you have one]
