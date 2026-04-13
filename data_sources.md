# Data Sources — Oil & Gas Monte Carlo Simulation

Channel parameters in `mc_simulation.py` trace to the sources listed here.
The paper (Oil & Gas: Combustion Floor) is available on SSRN and contains the full
reference list and §4 calibration narrative.

---

## Channel Sources

### `C1_co2_climate_damages`

CO₂ combustion damages at EPA SCC=$190/tCO₂. 18.5Gt CO₂/yr × $190 = $3.515T. Sources: EPA 2023 SCC, GIVE model (Rennert et al. 2022), IEA WEO.

*Full citations: paper §4 (available SSRN).*

### `C2_methane_operational`

Operational methane leakage at SC-CH₄=$1,600/t. 80-130Mt CH₄/yr. IEA: 75% eliminable at zero net cost. Sources: EPA SC-CH₄, IEA Methane Tracker, NOAA.

*Full citations: paper §4 (available SSRN).*

### `C3_air_pollution_health`

O&G share of $2.9T global fossil fuel air pollution cost (CREA). 7,500 US deaths from production alone. Cancer Alley: 47× EPA cancer threshold. Sources: CREA, BU/UNC 2023, Lancet.

*Full citations: paper §4 (available SSRN).*

### `C4_oil_spills_ecosystem`

Oil spills, pipeline leaks, ecosystem degradation, produced water contamination. Deepwater Horizon alone $65B+. Chronic low-level contamination. Sources: NOAA, API spill data, ITOPF.

*Full citations: paper §4 (available SSRN).*

### `C5_governance_resource_curse`

Resource curse GDP penalty (1.5% × $7T OPEC+ GDP = $105B), $452.6M Big Five lobbying 2011-2021, $7T global subsidies, API 1998 'Roadmap' disinformation. Sources: IMF, OpenSecrets, API.

*Full citations: paper §4 (available SSRN).*

### `C6_stranded_asset_risk`

Stranded assets: $16.1T cumulative over 25yr transition (annualized $644B). 60% valuation haircut under NZE ($2.1T market cap). Sources: IEA NZE, IMF, Carbon Tracker.

*Full citations: paper §4 (available SSRN).*

---

## Industry Revenue (Π)

The private payoff Π = $3,500.0B/yr is global annual industry revenue.
Source: paper §2 and §4. See paper §DA-1 (Decision Audit Field 7) for full
revenue source documentation.

---

## SAPM Framework

- Postnieks, E. (2026). *The Private Pareto Theorem*. SAPM Foundation Paper. SSRN.
- Postnieks, E. (2026). *Oil & Gas (Combustion Floor)*. SAPM Working Paper. SSRN.

---

## Distribution Methodology

- Iman, R. L., & Conover, W. J. (1982). A distribution-free approach to
  inducing rank correlation among input variables. *Communications in
  Statistics — Simulation and Computation*, 11(3), 311–334.
- Cooke, R. M. (1991). *Experts in Uncertainty*. Oxford University Press.
