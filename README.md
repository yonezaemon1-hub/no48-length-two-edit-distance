# No.48 - Exact Small-Alphabet Distortion and Strict Alphabet Dependence for Length-Two Edit Distance

**Ryutaro Yonezu - Independent Researcher**  
**Version:** v1.0 | **Date:** 2026-11-01  
**Proof:** Computer-assisted proof  
**Novelty:** INCONCLUSIVE | **Peer review:** Not human peer-reviewed  
**License:** All rights reserved

## Publication files

- [English preprint PDF](No48_Length_Two_Edit_Distance_v1_0.pdf)
- [Reproducibility ZIP](No48_Reproducibility_v1_0_20261101.zip)
- [SHA256 checksums](SHA256SUMS.txt)

To reproduce the proof, extract the ZIP and run the commands below from its No48_v1.0 directory. The code and certificates are contained in the ZIP.

## Scope and central results

Let D_q(2) be the minimum distortion into real l1 of unit-cost Levenshtein edit distance on all words of lengths 0, 1, and 2 over a q-letter alphabet (including the empty word).

- **D_4(2) = 123/101** (matching exact rational primal/dual certificates).
- **D_q(2) >= 785/643 for q >= 5**, so D_5(2) > D_4(2).
- Also certified: D_1(2)=1, D_2(2)=6/5, D_3(2)=17/14; D_q(2)<=9/7; and D_k(2)<=D_infinity(2)<=k D_k(2)/(k-1) for k>=2.

The exact values for q>=5 and for D_infinity(2) are **not determined**. No general optimum or priority claim is made.

## Prior work and attribution

Andoni, Deza, Gupta, Indyk, and Raskhodnikova (SODA 2003, pp. 523-526, DOI 10.1145/644108.644196) already use the finite-string cut-LP approach and report binary length-at-most-three distortion 4/3. Finite-string computation and cut decomposition are established methods. See PAPER_EN.md Section 7 for the precise overlap and the different finite spaces considered here.

OpenAI Math family 099 concerns asymptotic growth in maximum word length with alphabet-uniform bounds; this work fixes length at two and varies alphabet size. The present proof does not rely on the correctness of OpenAI's theorem. No affiliation or endorsement is asserted. Novelty remains INCONCLUSIVE.

## Reproduce the frozen certificates

```bash
bash verify_all.sh
```

Windows PowerShell 5.1:

```powershell
powershell -ExecutionPolicy Bypass -File .\verify_all.ps1
```

Python 3.10+ and a C++17 g++ compiler are required for the complete check. Core verification uses Python standard-library exact arithmetic. Missing g++ makes the complete audit fail closed. The optional independent q4 check requires NumPy:

```bash
python3 -I code/independent_q4_python.py
```

Generator and optimization scripts may need NumPy/SciPy; they are not required to check the frozen certificates and should not be run to overwrite evidence.

## Audit meaning and limits

The supplied independent AI audit reports PASS for v0.2. Release checks rerun all exact verifiers and the full 58,720,256-case q5 canonical enumeration, plus the independent Python q4 enumeration. These are computer-assisted checks, not human peer review or fully formal proof. An externally reported direct 2^30 q5 scan and mutation test are not bundled and were not repeated for this release. PASS does not establish novelty or priority.

All code/, evidence/, verify_all.sh, verify_all.ps1, and PROOF_AUDIT_EN.md are byte-for-byte unchanged from v0.2; the mathematical manuscript sections 1-6 are also unchanged in PAPER_EN.md. PROTECTED_V02_SHA256.json records the comparisons. SOURCE_ARCHIVE/ retains the original ZIP and its checksum. Historical audit files still say HOLD because they record the pre-publication state; this README, PAPER_EN.md and STATUS_AND_LIMITS.md govern v1.0.

## Files

- No48_Length_Two_Edit_Distance_v1_0.pdf - English preprint, identical to the standalone release PDF.
- PAPER_EN.md and source/paper.tex - manuscript sources.
- code/ and evidence/ - unchanged verification programs and frozen certificates.
- PROOF_AUDIT_EN.md - unchanged v0.2 trust-boundary notes.
- PUBLICATION_CHECKS.json and verification_logs/ - this release's checks.
- SHA256SUMS - exact inventory and hashes, excluding itself.

Copyright (c) 2026 Ryutaro Yonezu. **All rights reserved**.
