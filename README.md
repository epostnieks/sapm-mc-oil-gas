# SAPM Monte Carlo — Oil & Gas / Combustion Floor

**Public replication repository for quantitative results in:**

> Postnieks, E. (2026). *Oil & Gas (Combustion Floor).* SAPM Working Paper. SSRN.

This repository provides everything needed to independently reproduce, audit,
and extend the Monte Carlo simulation underlying the paper's core results.
The paper is available on SSRN.

---

## Results (N = 100,000 draws, seed = 42)

| Statistic | Value |
|-----------|-------|
| **β_W median** | **1.63** |
| β_W mean | 1.64 |
| β_W std | 0.2 |
| **90% CI** | **[1.3, 2.0]** |
| 99% CI | [1.2, 2.2] |
| P(β_W < 1) | 0.0010% |
| **ΔW median** | **$5,688.6B/yr** |
| Π (revenue) | $3,500.0B/yr |

**β_W = 1.63** means the oil & gas industry destroys **$1.63 in system
welfare for every $1.00 in revenue** — across 6 channels and 100,000 Monte Carlo draws.

**Classification**: Class 1 — Impossibility

---

## What Is β_W?

```
β_W = ΔW / Π
```

- **ΔW** = total annualized welfare destruction ($B/yr) across all channels
- **Π** = annual industry **revenue** ($B/yr) — not profit

β_W > 1: industry destroys more welfare than it captures in revenue.
β_W > 3: Strong Intractability threshold — reform requires structural replacement.

---

## Quick Start

```bash
git clone https://github.com/epostnieks/sapm-mc-oil-gas.git
cd sapm-mc-oil-gas
pip install numpy scipy
python mc_simulation.py
```

Expected output: `β_W median : 1.63` and `ΔW median : $5,688.6B/yr`

---

## Welfare Channels

| Channel | Median ($B/yr) | 90% CI | Distribution |
|---------|---------------|--------|--------------|
| C1_co2_climate_damages | $3,512.8B | [$2,925.4B, $4,215.1B] | Lognormal |
| C2_methane_operational | $127.9B | [$88.5B, $185.5B] | Lognormal |
| C3_air_pollution_health | $979.6B | [$640.5B, $1,499.2B] | Lognormal |
| C4_oil_spills_ecosystem | $120.1B | [$71.9B, $199.7B] | Lognormal |
| C5_governance_resource_curse | $249.5B | [$156.5B, $398.6B] | Lognormal |
| C6_stranded_asset_risk | $643.3B | [$415.1B, $999.9B] | Lognormal |
| **Total ΔW** | **$5,688.6B** | **[$4,679.7B, $6,942.8B]** | Correlated (ρ=0.3) |

---

## Impossibility Floor

The floor β_W ≥ 1.0 cannot be breached by any policy while the
industry continues to operate. In 100,000 draws, only **0.0010%**
fall below this floor — confirming the structural constraint.

## Repository Contents

| File | Description |
|------|-------------|
| `mc_simulation.py` | Self-contained simulation — no private pipeline imports |
| `mc_results.json` | Pre-run results (100K draws, seed=42) — matches paper |
| `mc_histogram.json` | Binned β_W distribution (80 bins) for companion chart |
| `assumptions.md` | Every parameter: value, derivation, source |
| `data_sources.md` | Full citation list for all empirical inputs |

---

## Replication Notes

Results are seeded and deterministic. Tested with:
```
numpy==1.26.4  scipy==1.12.0  Python 3.11.9
```

The `median` and `ci_90` (to 1 decimal) match exactly across compatible versions.

---

## License

CC BY 4.0. Cite as:

> Postnieks, E. (2026). *SAPM Monte Carlo — Oil & Gas (Combustion Floor)*.
> GitHub: epostnieks/sapm-mc-oil-gas.
> https://github.com/epostnieks/sapm-mc-oil-gas
