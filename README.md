# ITIS 3200 – Group 14: IMUNES Network Segmentation Hardening

## Project Overview
This repository supports our ITIS 3200 course project on **Network Segmentation Hardening** against lateral movement from a compromised IoT device to a sensitive workstation using **IMUNES**[cite: 1, 2].

## Group Seed & Parameters
* **Formula:** `(Sum of 4 Members' Student ID Last 2 Digits) mod 18`[cite: 2]
* **Calculation:** `(20 + 34 + 23 + 04) mod 18 = 81 mod 18 = 9`[cite: 2, 6]
* **Group Seed:** `9`[cite: 2, 6]

## Planned Structure
* `topologies/` — IMUNES (`.imn`) network topologies (flat baseline and segmented)[cite: 2]
* `scripts/` — Setup, `iptables` firewall rules, and verification/test scripts[cite: 2]
* `evidence/` — Captured command outputs and test results[cite: 1, 2]
* `docs/` — Project notes, proposal, and report drafts[cite: 1, 2]

## States to Demonstrate
1. **Broken / Flat Baseline:** All nodes on a single unsegmented network with no cross-traffic restrictions, allowing lateral movement (`nmap` discovery and workstation service access) from the compromised IoT host[cite: 2].
2. **Hardened / Segmented State:** Isolated segments/VLANs with `iptables` default `DROP` on cross-segment forwarding and only the seed-scoped management exception allowed[cite: 2].
