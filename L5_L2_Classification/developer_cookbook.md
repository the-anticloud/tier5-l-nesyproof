# Developer Cookbook — L_NESYPROOF
**Stack:** Python 3.11, PAX 27B, Lean 4 / Coq (formal proof), pyswip, AIOSS_FORMAT
**Domain:** NeSyProof: neuro-symbolic proof generation and verification for Anticloud reasoning

## Generate and verify formal proof
```python
from l_nesyproof import NeSyProof

prover = NeSyProof(
    pax_model="./pax-27b-q4.gguf",
    proof_engine="lean4",
    aioss_chain="./nesyproof.aioss"
)

result = prover.prove(
    claim="The AIOSS chain append function is collision-resistant under SHA3-256",
    context="SHA3-256 is a collision-resistant hash function per NIST SP 800-185"
)
print(f"Proved: {result.proved}")
print(f"Lean4 proof:\n{result.lean4_code}")
print(f"Verification: {result.lean4_verified}")
print(f"Certificate chain: {result.chain_hash}")
```

## Batch prove regulatory claims
```python
claims = [
    "AIOSS chain entries are temporally ordered",
    "Chain append is an atomic operation",
    "Chain hash is deterministic given same inputs"
]
proofs = prover.batch_prove(claims)
for claim, proof in zip(claims, proofs):
    print(f"{'PROVED' if proof.proved else 'FAILED'}: {claim[:60]}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
