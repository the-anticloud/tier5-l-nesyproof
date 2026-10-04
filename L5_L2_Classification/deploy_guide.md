# Deploy Guide — L_NESYPROOF
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PAX 27B, Lean 4 / Coq (formal proof), pyswip, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PAX 27B, Lean 4 (separate install), pyswip 0.3+.

## Environment
Lean 4 requires separate installation. 8GB RAM. GPU for PAX sketch generation. CPU for formal verification.

## AIOSS Integration
```bash
aioss init --module L_NESYPROOF --output ./l_nesyproof.aioss
aioss append --chain ./l_nesyproof.aioss --payload ./output.bin --module L_NESYPROOF
aioss verify --chain ./l_nesyproof.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_NESYPROOF",
    aioss_chain="./L_NESYPROOF.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_NESYPROOF.aioss --verbose
python -m L_NESYPROOF.tests.smoke
```
