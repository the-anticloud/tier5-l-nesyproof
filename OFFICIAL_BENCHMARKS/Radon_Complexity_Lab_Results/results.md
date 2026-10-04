# Radon_Complexity_Lab_Results
**Project:** `L_NESYPROOF` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `7`
- **average_complexity:** `{'grade': 'A', 'score': 4.495412844036697}`
- **complexity_grade:** `A`
- **complexity_score:** `4.495412844036697`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_NESYPROOF\UPSTREAM\_anticloud_egress.py - A (79.55)
E:\fe`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_NESYPROOF\UPSTREAM\_anticloud_egress.py
    F 38:0 _is_frontier - A (4)
    F 43:0 guarded_connect - A (4)
    F 61:0 install - A (3)
    F 33:0 is_offline - A (1)
    C 29:0 EgressDenied - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_NESYPROOF\UPSTREAM\prototype\hybrid_reasoner.py
    M 417:4 HybridTemporalReasoner._compute_symbolic_answer - C (13)
    M 240:4 HybridTemporalReasoner._verification_step - B (8)
    M 292:4 HybridTemporalReasoner._generate_final_answer - B (6)
    C 37:0 HybridTemporalReasoner - A (5)
    M 127:4 HybridTemporalReasoner._detect_reasoning_level - A (5)
    M 342:4 HybridTemporalReasoner._parse_time_value - A (5)
    M 142:4 HybridTemporalReasoner._llm_extraction_step - A (4)
    M 181:4 HybridTemporalReasoner._symbolic_conversion_step - A (4)
    M 328:4 HybridTemporalReasoner._convert_event_to_interval - A (4)
    M 363:4 HybridTemporalReasoner._parse_duration - A (4)
    M 59:4 HybridTemporalReasoner.reason - A (3)
    M 208:4 HybridTemporalReasoner._symbolic_reasoning_step - A (3)
    M 455:4 HybridTemporalReasoner.compare_with_pure_llm - A (2)
    C 22:0 HybridResult - A (1)
    M 47:4 HybridTemporalReasoner.__init__ - A (1)
    M 391:4 HybridTemporalReasoner._convert_to_allen_relation - A (1)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_NESYPROOF\UPSTREAM\prototype\llm_interface.py
    M 131:4 MockLLM._handle_medical_timeline - C (15)
   
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_