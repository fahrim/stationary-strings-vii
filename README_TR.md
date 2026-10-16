# Duran Sicimler Teoremi VII — Yayın Paketi

> **English:** [README.md](./README.md)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23427566.svg)](https://doi.org/10.5281/zenodo.23427566)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

**Duran Sicimler Teoremi VII: CERN ALPHA Antimadde Tuzaklarında Öz-Tutarlı Girdap Doyumu, İlk-İlkelerden Hiperince Rezonans Çizgi Şekli ve 511 keV Ore–Powell Spektrum Çözümü**

Yazar: Fahri Meral · Tarih: 17 Ekim 2026 · Sürüm: v1 (Makale VII)

> **Durum:** Yayımlanmamış ön baskı (v1). Hakem denetiminden geçmemiştir.

## İçerik

| Dosya | Açıklama |
|---|---|
| `paper/duran_sicimler_teoremi_VII.tex` | Ana makale, Türkçe (Tablo 1–4, Şekil 1 2×2) |
| `paper/duran_sicimler_teoremi_VII_EN.tex` | İngilizce sürüm |
| `figs/fig9_cern_alpha_trap_and_511keV_exact.pdf` | Test T16–T19 şekli (TR, 2×2) |
| `figs/fig9_cern_alpha_trap_and_511keV_exact.png` | Test T16–T19 şekil önizlemesi (TR) |
| `figs/fig9_cern_alpha_trap_and_511keV_exact_en.pdf` | Test T16–T19 şekli (EN, 2×2) |
| `figs/fig9_cern_alpha_trap_and_511keV_exact_en.png` | Test T16–T19 şekil önizlemesi (EN) |
| `CITATION.cff` | Atıf kaydı |
| `LICENSE` | MIT |

## Sayısal üretim

Test T16–T19, **V. makale deposundaki** ([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)) çözücüyle üretilir:

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T19 (19/19 PASS)
python duran_sicimler_sim/generate_figures.py  # Şekil 1 (+_en)
```

## Kilit bulgular

- T16: SDR-EVC tork uyuşmazlığı (`r_p^ideal = 0,0989 mm → r_p^exp = 0,16 mm`,
  `μ_s* = 0,20317683698063987`); sıfır-parametreli `μ_s^Meral = 2√2 Λ_Meral^(0) = 0,204409`
  (%0,61 uyum, `r_p = 0,16079 mm`) ve örneklem-dışı `e⁺` çapraz doğrulaması
  (`r_p^eff(e⁺) = 0,4517 mm ∈ [0,30; 0,50] mm`); cıvıltı kazancı `1,0893745115`.
- T17: `1,03/1,07 T` çift-alan sürüklenmesi (`-2,599/-2,700 µT/saat`, ECR
  `-2,50/-2,60 ± 0,10 µT/saat` ile `1σ` uyum), sıfır-parametreli oran `|R_th − R_exp| = 1,28e-4`;
  analitik `g_vortex` (eşikte `x^2`, arada `x^-1,9010`, `+4,65 kHz` kayma).
- T18: tam 1949 Ore–Powell düzeltmesi (`ln(1−x)` geri konuldu; `O_exact(0) = 0`,
  `∫_0^m = 0,9999999999995262`); 3 galaktik rejim (`8,0e-8`, `2,0e-7`, `4,0e-7 M☉/yıl`).
- T19: CERN BASE-STEP 2026 karayolu taşıması (`92` antiproton, `7,5 km / 24 dk`,
  `ΔC = 20 fF / Δf = 122 Hz`) — Teorem 5 FENE-P Lyapunov kararlılığı (`r_-^max = 0,153 µm`,
  `92/92 = %100` hayatta kalma, `M_safety = 2,55e7`).

## Alıntı

```bibtex
@misc{meral2026duranVII,
  author = {Fahri Meral},
  title  = {Duran Sicimler Teoremi VII: CERN ALPHA Antimadde Tuzaklarında Öz-Tutarlı Girdap Doyumu, İlk-İlkelerden Hiperince Rezonans Çizgi Şekli ve 511 keV Ore-Powell Spektrum Çözümü},
  year   = {2026},
  doi    = {10.5281/zenodo.23427566},
  url    = {https://github.com/fahrim/stationary-strings-vii}
}
```

`CITATION.cff` dosyasına da bakınız.

## Lisans

MIT — bkz. `LICENSE`. İçerik hakem denetiminden geçmemiştir.
