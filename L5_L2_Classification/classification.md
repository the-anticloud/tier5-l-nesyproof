# L5 Narrow / L2 General Classification — L_NESYPROOF
**Platform:** Anticloud | **Tier:** TIER_5_WORLD_NEURO_EMBODIED | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
L_NESYPROOF generates formal mathematical proofs from PAX 27B's reasoning steps. Narrow scope: Anticloud domain logical claims — AIOSS chain correctness proofs, safety property proofs for TIER_9 robotics, and regulatory compliance formal proofs.

## L2 General
L2 General: L_NESYPROOF provides formal verification for any tier's critical logical claims. TIER_9 collision avoidance properties and TIER_7 dosing safety properties both get Lean 4 verified proofs.

## PAX 27B Integration
PAX 27B generates proof sketch and key lemmas in natural language; L_NESYPROOF translates these into Lean 4/Coq syntax and verifies them. AIOSS-chained proofs are tamper-evident certification artifacts.

## AIOSS Audit Chain
Every proof artifact (claim hash + proof sketch hash + Lean4 code hash + verification result + proof certificate hash) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
ISO/IEC 42001 (verifiable AI reasoning). NIST AI RMF 1.0 (explainable AI).
