# HF_Leaderboard_Lab_Results

**Project:** `L_NESYPROOF`  
**Tier:** `TIER_5_WORLD_NEURO_EMBODIED`  
**Slug:** `o2alexanderfedin/provenance-neurosymbolic-verification`  
**Commit:** `b9be6c805fc3`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **43.34 ms** |
| Min latency | 40.49 ms |
| Max latency | 48.49 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **47** |
| Tokenization latency | 2.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5808 |
| Classification latency | 81.52 ms |
| Status | **PASS** |

**Input text tokenized:**
```
L_NESYPROOF (o2alexanderfedin/provenance-neurosymbolic-verification) — 62 files, 2771 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'l', '_', 'nes', '##yp', '##ro', '##of', '(', 'o', '##2', '##ale', '##xa', '##nder', '##fed', '##in', '/', 'proven', '##ance', '-', 'ne']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_