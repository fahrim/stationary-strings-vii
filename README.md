# Stationary Strings Theorem VII — Publication Package

> **Türkçe:** [README_TR.md](./README_TR.md)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23427566.svg)](https://doi.org/10.5281/zenodo.23427566)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

**Stationary Strings Theorem VII: Self-Consistent Vortex Saturation in CERN ALPHA Antimatter Traps, First-Principles Hyperfine Lineshape Derivation, and the Exact 511 keV Ore–Powell Spectrum Resolution**

Author: Fahri Meral · Date: October 17, 2026 · Version: v1 (Paper VII)

> **Status:** Unpublished preprint (v1). Not peer-reviewed.

## Contents

| File | Description |
|---|---|
| `paper/duran_sicimler_teoremi_VII.tex` | Main paper, Turkish (Tables 1–4, Figure 1 2×2) |
| `paper/duran_sicimler_teoremi_VII_EN.tex` | English version |
| `figs/fig9_cern_alpha_trap_and_511keV_exact.pdf` | Tests T16–T19 figure (TR, 2×2) |
| `figs/fig9_cern_alpha_trap_and_511keV_exact.png` | Tests T16–T19 figure preview (TR) |
| `figs/fig9_cern_alpha_trap_and_511keV_exact_en.pdf` | Tests T16–T19 figure (EN, 2×2) |
| `figs/fig9_cern_alpha_trap_and_511keV_exact_en.png` | Tests T16–T19 figure preview (EN) |
| `CITATION.cff` | Citation record |
| `LICENSE` | MIT |

## Numerical reproduction

Tests T16–T19 are produced with the solver in the **Paper V repository**
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)):

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T19 (19/19 PASS)
python duran_sicimler_sim/generate_figures.py  # Figure 1 (+_en)
```

## Key findings

- T16: SDR-EVC torque discrepancy resolved (`r_p^ideal = 0.0989 mm → r_p^exp = 0.16 mm`,
  `μ_s* = 0.20317683698063987`); zero-parameter `μ_s^Meral = 2√2 Λ_Meral^(0) = 0.204409`
  (0.61% match, `r_p = 0.16079 mm`) and out-of-sample `e⁺` cross-validation
  (`r_p^eff(e⁺) = 0.4517 mm ∈ [0.30, 0.50] mm`); chirp gain `1.0893745115`.
- T17: `1.03/1.07 T` dual-field drift (`-2.599/-2.700 µT/h`, within `1σ` of ECR
  `-2.50/-2.60 ± 0.10 µT/h`), zero-parameter ratio `|R_th − R_exp| = 1.28e-4`;
  analytic `g_vortex` (threshold `x^2`, mid-tail `x^-1.9010`, `+4.65 kHz` shift).
- T18: exact 1949 Ore–Powell correction (`ln(1−x)` restored; `O_exact(0) = 0`,
  `∫_0^m = 0.9999999999995262`); 3 Galactic regimes (`8.0e-8`, `2.0e-7`, `4.0e-7 M☉/yr`).
- T19: CERN BASE-STEP 2026 road transport (`92` antiprotons, `7.5 km / 24 min`,
  `ΔC = 20 fF / Δf = 122 Hz`) — Theorem 5 FENE-P Lyapunov stability (`r_-^max = 0.153 µm`,
  `92/92 = 100%` survival, `M_safety = 2.55e7`).

## Citation

```bibtex
@misc{meral2026duranVII,
  author = {Fahri Meral},
  title  = {Stationary Strings Theorem VII: Self-Consistent Vortex Saturation in CERN ALPHA Antimatter Traps, First-Principles Hyperfine Lineshape Derivation, and the Exact 511 keV Ore-Powell Spectrum Resolution},
  year   = {2026},
  doi    = {10.5281/zenodo.23427566},
  url    = {https://github.com/fahrim/stationary-strings-vii}
}
```

See also `CITATION.cff`.

## License

MIT — see `LICENSE`. Content is not peer-reviewed.
