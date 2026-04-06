# AI-Based Preventive Maintenance of Equipment and Demand Forecast of Spares

> **Conference Paper | LEAD 2025 | BITS Pilani**  
> Thilak S · Aditya Raj · Bharat Raj Singal · Dr. Phaneendra Kiran Chaganti  
> Department of Mechanical Engineering, BITS Pilani, Pilani Campus  
> `{f20220771, f20221583, f20221151}@pilani.bits-pilani.ac.in` · `cpkiran@hyderabad.bits-pilani.ac.in`

A **Random Forest + Linear Regression** AI framework for defence supply chain risk quantification, geopolitical scenario modelling, and spare parts demand forecasting across India's critical military platforms — S-400 Triumf, Rafale Fighter Jet, AH-64E Apache, Barak Missiles, and K9 Thunder Artillery.

![AI/ML](https://img.shields.io/badge/-AI%20%2F%20ML-e07b39?style=flat-square)
![Supply Chain](https://img.shields.io/badge/-Supply%20Chain-2e4057?style=flat-square)
![Defence Logistics](https://img.shields.io/badge/-Defence%20Logistics-1a1a2e?style=flat-square)
![Python](https://img.shields.io/badge/-Python-3776ab?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/-scikit--learn-f7931e?style=flat-square)

---

## Abstract

India's defence procurement has shifted significantly — from 72% Russian sourcing (2010–2014) to a distributed multi-partner model involving France (28%), Israel (15%), and the USA (7–12%) by 2020–2024. While diversification reduces single-source risk, it introduces complex multi-tier vulnerabilities that demand more sophisticated management tools.

This paper presents an AI-based framework for preventive maintenance and demand forecasting that builds resilience in India's defence supply chains through systematic vulnerability assessment and operationalization of geopolitical risk. A **holistic multi-tier supply chain mapping** was developed for five critical platforms. The risk scoring model integrates data from the **Correlates of War (COW) Project** and **Uppsala Conflict Data Programme (UCDP)** to objectively generate risk outputs using:

- **Random Forest** (30 estimators, max depth 6) — conflict risk prediction
- **Linear Regression** — EU export restriction likelihood estimation

The model identified that **"Last Conflict Year"** (56.1% importance) and **"Militarized Disputes Count"** (39.1% importance) are the dominant predictors of supply disruption risk. Russian suppliers received the highest risk scores (7.5–8.2); South Korean suppliers the lowest (2.1–2.8). The framework predicted S-400 delivery disruptions months before they materialized following the Russia–Ukraine conflict, validating its early warning capability.

**Keywords:** Defence supply chain · AI-based risk assessment · Preventive maintenance · Geopolitical risk simulation · Multi-tier mapping · Demand forecasting · Random Forest · India

---

## Motivation

India maintains approximately **60% of its military inventory in Russian-origin equipment** — all requiring continuous spares, maintenance, and technical support. The Russia–Ukraine conflict and subsequent Western sanctions created real-world supply shocks (S-400 delivery delays on a $5.5 billion deal) that exposed the critical gap between theoretical supply chain vulnerability and actual operational impact.

**Why traditional approaches fall short:**

- **Reactive maintenance** — equipment downtime is discovered only at failure; no predictive horizon for spare demand
- **Single-source dependency** — Almaz-Antey as sole supplier for S-400 systems creates cascading risk with no alternative routing
- **Static risk models** — geopolitical disruptions are treated as binary events, not probabilistic continuous signals
- **Absent supply chain visibility** — most vulnerability lies in invisible Tier 2/3 suppliers (e.g., Hyundai WIA for K9 armament, STX Engine for K9 powertrain) not tracked in procurement databases
- **Technology transfer gaps** — S-400 JV limitations mean India cannot self-sustain critical components, unlike Apache (exclusive fuselage production at TBAL, Hyderabad)
- **Data silos** — maintenance logs, geopolitical feeds, and procurement data are not integrated into a single risk-aware forecasting pipeline

---

## Key Results

| Metric | Value |
|--------|-------|
| **Model** | Random Forest (30 estimators, max depth 6) + Linear Regression |
| **Top feature — Conflict Risk** | Last Conflict Year — 56.1% importance |
| **2nd feature — Conflict Risk** | Militarized Disputes Count — 39.1% importance |
| **Russia risk score** | 7.5–8.2 / 10 |
| **South Korea risk score** | 2.1–2.8 / 10 |
| **Sample prediction (conflict risk)** | 8.19 / 10 |
| **Sample prediction (EU export restriction)** | 5.92 / 10 |
| **Semiconductor alt. sourcing — Taiwan** | Lead time: 3 weeks |
| **Semiconductor alt. sourcing — South Korea** | Lead time: 4 weeks |
| **Semiconductor alt. sourcing — USA** | Lead time: 5 weeks |
| **Iran–Regional instability correlation** | r = 0.74 |
| **Early warning advantage** | 24–48 hours ahead of traditional intelligence |

---

## Critical Systems Analysed

| System | Country of Origin | Primary Manufacturer | Ownership | Indian Involvement |
|--------|------------------|---------------------|-----------|-------------------|
| S-400 Triumf | Russia | Almaz-Antey | State-owned (Rostec) | Local JV for spares planned |
| Rafale Fighter Jet | France | Dassault Aviation | Public (Dassault Group 50.55%) | Fuselage by TASL; 36 jets delivered |
| AH-64E Apache | USA | Boeing | Public (Institutional majority) | TBAL — exclusive global Apache fuselage manufacturer |
| Barak Missiles | Israel | Israel Aerospace Industries (IAI) | State-owned | KRAS JV — MRSAM kits for Army/Air Force + export |
| K9 Thunder Artillery | South Korea | Hanwha Aerospace | Public (36% public, 36% individual) | K9 Vajra-T by L&T; >50% local content |
| Su-30MKI Fighter | Russia | Sukhoi (UAC) | Russian State-owned | Majority assembled by HAL |

---

## Multi-Tier Supply Chain Mapping

| System | Component | Tier | Supplier | Country | Ownership | Indian Role |
|--------|-----------|------|----------|---------|-----------|-------------|
| S-400 | Complete System | Tier 1 | Almaz-Antey | Russia | State-owned | JV for spares planned |
| S-400 | 91N6E "Big Bird" Radar | Tier 2 | Almaz-Antey | Russia | State-owned | — |
| Rafale | Complete System | Tier 1 | Dassault Aviation | France | Public | 36 jets delivered |
| Rafale | Landing Gears, Brakes | Tier 2 | Safran Landing Systems | France | Public (diverse) | — |
| Rafale | Fuselage Sections | Tier 2 | TASL | India | Private (Tata Sons) | Exclusive Rafale fuselage outside France |
| Apache | Complete System | Tier 1 | Boeing | USA | Public (institutional) | 22 aircraft received |
| Apache | Fuselage | Tier 2 | Tata Boeing Aerospace (TBAL) | India | JV (TAS–Boeing) | **Exclusive global AH-64 fuselage manufacturer** |
| Apache | GE T700 Engines | Tier 2 | General Electric | USA | Public (institutional) | — |
| Apache | LONGBOW Radar | Tier 2 | Longbow LLC (Lockheed–Northrop JV) | USA | Public (institutional) | — |
| Apache | TADS/PNVS System | Tier 2 | Lockheed Martin MFC | USA | Public (institutional) | — |
| Barak | Complete System | Tier 1 | IAI | Israel | State-owned | Joint development with DRDO |
| Barak | MRSAM Kits | Tier 2 | Kalyani Rafael Advanced Systems | India | JV (Kalyani–Rafael) | Manufacture for Army/Air Force + export |
| Barak | Missile Components | Tier 3 | Rafael Advanced Defence Systems | Israel | State-owned | — |
| K9 | Complete System | Tier 1 | Hanwha Aerospace | South Korea | Public | Assembled as K9 Vajra-T by L&T |
| K9 | Main Armament (CN98) | Tier 2 | Hyundai WIA | South Korea | Public (Hyundai Motor 40.74%) | — |
| K9 | Engine | Tier 2 | STX Engine / MTU Friedrichshafen | S. Korea | Public (institutional) | — |
| K9 | Transmission | Tier 2 | SNT Dynamics / Allison Transmission | S. Korea / USA | Public (institutional) | — |

---

## Vulnerability Assessment

| System | Critical Component | Primary Supplier | Key Vulnerabilities | Risk Level |
|--------|--------------------|-----------------|---------------------|------------|
| S-400 | Complete System, Radar | Almaz-Antey (Russia) | Single-source; sanctions exposure; state-owned; ongoing conflict | ![HIGH](https://img.shields.io/badge/-HIGH-red?style=flat-square) |
| Rafale | Landing Gears, Fuselage | Safran, Dassault, TASL | Tier 2/3 dependencies; mitigated by co-production | ![MODERATE](https://img.shields.io/badge/-MODERATE-orange?style=flat-square) |
| Apache | Engines, Radar, Targeting | GE, Longbow LLC, Lockheed Martin | Multi-tier foreign dependency; US policy sensitivities | ![MODERATE](https://img.shields.io/badge/-MODERATE-orange?style=flat-square) |
| Barak | Missile Kits, Components | IAI, KRAS | State-owned reliance; regional instability; mitigated by JV | ![LOW-MODERATE](https://img.shields.io/badge/-LOW--MODERATE-yellow?style=flat-square) |
| K9 | Armament, Engine, Transmission | Hanwha, Hyundai WIA, STX | Multi-tier foreign dependency; mitigated by high local content | ![LOW](https://img.shields.io/badge/-LOW-brightgreen?style=flat-square) |

---

## AI Risk Scoring Model

### Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                        INPUT FEATURES                               │
│   hezbollah_mentions    iran_threat_level                           │
│   gaza_tension_index    domestic_politics_crisis                    │
└────────────────────────┬────────────────────────────────────────────┘
                         │
          ┌──────────────┴──────────────┐
          ▼                             ▼
┌──────────────────┐          ┌──────────────────────┐
│  RandomForest    │          │   LinearRegression   │
│  n_est=30        │          │   sklearn             │
│  max_depth=6     │          │                      │
│  random_state=42 │          │                      │
└────────┬─────────┘          └──────────┬───────────┘
         ▼                               ▼
 conflict_risk (0-10)        eu_export_block_score (0-10)
```

### Geopolitical Risk Factor Weighting

| Risk Factor | Weight (%) | Data Source | Rationale |
|-------------|-----------|-------------|-----------|
| Last Conflict Year | **56.1** | COW MID v5.0 | Recency of conflict is the strongest predictor of recurrence risk |
| Militarized Disputes Count | **39.1** | COW MID v5.0 | Historical frequency of instability |
| Defence Cooperation | 2.6 | Bilateral agreements | Reduces risk via formal collaboration |
| Formal Alliance | 2.2 | COW Alliances dataset | Mutual support provides marginal protective effect |

---

## Governing Equations & Model Details

### Random Forest Ensemble (Breiman, 2001)

$$\hat{y} = \frac{1}{T} \sum_{t=1}^{T} h_t(\mathbf{x})$$

where $h_t(\mathbf{x})$ is the prediction of the $t$-th tree for input $\mathbf{x}$. $T = 30$, max depth = 6.

### Feature Importance (Mean Decrease Impurity)

$$\text{Importance}(f) = \frac{1}{T} \sum_{t=1}^{T} \sum_{n \in \text{nodes splitting on } f} w_n \cdot \Delta I_n$$

### Linear Regression — EU Export Risk

$$\hat{y}_{\text{eu}} = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \beta_3 x_3 + \beta_4 x_4$$

where $x_1$ = hezbollah_mentions, $x_2$ = iran_threat_level, $x_3$ = gaza_tension_index, $x_4$ = domestic_politics_crisis.

### Risk Score Normalization

- **0–3**: Low risk — standard procurement pathway
- **3–5**: Low-to-moderate — monitor and prepare contingency
- **5–7**: Moderate — activate secondary sourcing
- **7–10**: High — trigger emergency alternative sourcing

---

## Data Sources

| Dataset | File | Organization | Usage |
|---------|------|-------------|-------|
| Militarized Interstate Disputes (MID) v5.0 | `MIDIP_COW.csv` | Correlates of War Project | Bilateral dispute history; last conflict year and dispute count per supplier country |
| Formal Alliances | `alliance_COW.csv` | Correlates of War Project | Alliance depth between India and supplier nations (1816–2012) |
| Defence Cooperation | `defence_cooperation_COW.csv` | Correlates of War Project | Bilateral defence cooperation agreements (1980–2010) |
| Country Codes | `COW-country-codes.csv` | Correlates of War Project | Standardized country code lookup for all bilateral computations |
| UCDP/PRIO Armed Conflict Dataset | — | Uppsala Conflict Data Programme | Organized violence and sub-national instability |
| SIPRI Arms Transfer Database | — | SIPRI | Global arms import/export trends |
| Company Annual Reports | — | Dassault, Boeing, Hanwha, L&T, TASL, Safran, et al. | JV structures, production capacities, strategic partnerships |

> The four COW CSV files must be downloaded from the [Correlates of War Project](https://correlatesofwar.org/) and placed in the root directory before running the notebook.

---

## Code Implementation

The full implementation is in [`COW.ipynb`](COW.ipynb) across five stages:

**Stage 1 — MID Dispute Analysis (`MIDIP_COW.csv`)**
Filters India-specific disputes (country code 750), computes bilateral severity with time-decay weighting, extracts `last_conflict_year` and `militarized_disputes_count` per supplier country.

**Stage 2 — Alliance Data (`alliance_COW.csv`)**
Filters India's alliance partners (1816–2012), checks for formal alliances with each supplier nation.

**Stage 3 — Defence Cooperation (`defence_cooperation_COW.csv`)**
Filters India-specific bilateral defence cooperation records, flags active cooperation per country.

**Stage 4 — Master Table (`COW-country-codes.csv`)**
Merges all four COW datasets into a unified feature table: `militarized_disputes`, `last_conflict_year`, `formal_alliance`, `defence_cooperation`.

**Stage 5 — Risk Prediction & Ranking**
Trains Random Forest (30 estimators, max depth 6) on the master table. Outputs feature importances and a ranked risk table for all supplier countries.

```python
# Bilateral severity with time-decay weighting
def calculate_bilateral_severity(country_code, decay_rate=0.1,
                                  current_year=2025, random_state=None):
    ...

# Merge all COW datasets into master table
def create_master_table(df):
    ...

# Risk prediction and ranking
def predict_and_rank_conflict_risk(master_df):
    conflict_model = RandomForestRegressor(
        n_estimators=30, max_depth=6, random_state=42
    )
    conflict_model.fit(X, y)
    ...
```

See [`COW.ipynb`](COW.ipynb) for the complete implementation with all outputs.

---

## Repository Structure

```
ai-defence-supply-chain/
├── COW.ipynb                        # Complete analysis notebook (all 5 pipeline stages)
├── MIDIP_COW.csv                    # COW Militarized Interstate Disputes (MID v5.0)
├── alliance_COW.csv                 # COW Formal Alliances (1816-2012)
├── defence_cooperation_COW.csv      # COW Defence Cooperation (1980-2010)
├── COW-country-codes.csv            # COW country code lookup
└── README.md
```

> **Note:** The four CSV files are sourced from the [Correlates of War Project](https://correlatesofwar.org/) and must be placed in the root directory before running the notebook.

---

## Alternative Sourcing Recommendations

| System | Vulnerable Component | Risk | Recommended Strategy |
|--------|---------------------|------|---------------------|
| S-400 | Radar, Missile Spares | ![HIGH](https://img.shields.io/badge/-HIGH-red?style=flat-square) | Domestic JV + diversified foreign sourcing |
| Rafale | Engine Components, Avionics | ![MODERATE](https://img.shields.io/badge/-MODERATE-orange?style=flat-square) | Deepen co-development; strategic stockpiling |
| Apache | Engine, Radar, Targeting Spares | ![MODERATE](https://img.shields.io/badge/-MODERATE-orange?style=flat-square) | Diversified foreign sourcing; develop domestic MRO |
| Barak | Missile Kits, Components | ![LOW-MOD](https://img.shields.io/badge/-LOW--MOD-yellow?style=flat-square) | KRAS JV expansion; strategic stockpiling |
| K9 | Armament, Engine, Transmission | ![LOW](https://img.shields.io/badge/-LOW-brightgreen?style=flat-square) | Expand domestic content beyond 60% |

---

## Strategic Implications

**Legacy Dependency — S-400 Triumf:** Single foreign supplier, no meaningful technology transfer, complete vulnerability to geopolitical disruption. Western sanctions on Russia directly caused multi-year delivery delays on a $5.5 billion deal.

**Transitional Integration — Rafale:** TASL produces the first Rafale fuselage outside France. A shift from procurement to industrial participation.

**Advanced Partnership — Apache:** TBAL in Hyderabad is the **exclusive global manufacturer** of AH-64 Apache fuselages for all Boeing customers worldwide. India has moved from end-consumer to a critical node in a Western OEM's global supply chain.

> Technology transfer depth — not procurement volume — is the primary determinant of long-term supply chain resilience.

---

## Novel Contributions

1. First structured multi-tier mapping of India's five critical defence platforms using OSINT
2. Objective, data-driven geopolitical AI risk engine using COW and UCDP structured datasets
3. Predictive validation — model flagged elevated Russian supplier risk ahead of S-400 delivery disruptions
4. First classification of defence supplier risk by ownership structure (state-owned vs. public vs. mixed)
5. Technology transfer depth demonstrated as the primary resilience metric — directly policy-actionable
6. Automated alternative sourcing engine with lead time, bilateral trade, and regulatory risk factoring

---

## Future Research Directions

- Real classified data integration through secure collaboration with Indian Army stakeholders
- Broader platform coverage — Scorpene submarines, INS Vikrant carrier air wing, Tejas, Arjun Mk2
- NLP-enhanced real-time risk monitoring from defence journals and diplomatic communiqués
- Spare demand surge modelling linking risk scores to probabilistic stockpile optimization
- Digital twin integration for real-time failure prediction
- Multi-objective optimisation across stockpile cost, operational unavailability risk, and foreign dependency

---

## References

1. Stanton et al. Predictive maintenance analytics for aircraft. *Systems Engineering*, 26(1), 2023.
2. Ochando et al. Data acquisition for condition monitoring in tactical vehicles. *Sensors*, 23(12), 2023.
3. Simion et al. AI-driven predictive maintenance in maritime transport. *Applied Sciences*, 14(20), 2024.
4. Kalafatelis et al. Predictive maintenance in the maritime industry. *JMSE*, 13(3), 2025.
5. Choi & Suh. Forecasting spare parts demand of military aircraft. *Sustainability*, 12(15), 2020.
6. Kim & Kim. Demand forecasting of spare parts using AI. *Mathematics*, 11(3), 2023.
7. Kim, Hwang & Doh. Predictive model with data scaling for spare parts. *Defence Science Journal*, 73(6), 2023.
8. Sharma, Ansar & Parkhe. Inventory woes in Indian defence SCM. *Defense and Security Studies*, 6(1), 2025.
9. Singh. Atmanirbharta Bharat: Supply chain resilience. *Journal of Defence Studies*, 18(4), 2024.
10. Elvemo. Supply chain resilience in military operations. *Scandinavian Journal of Military Studies*, 8(1), 2025.
11. Singer & Bremer. Interstate war: An event-data approach. *Journal of Conflict Resolution*, 32(2), 1988.
12. Sundberg & Melander. UCDP Georeferenced Event Dataset. *Journal of Peace Research*, 50(4), 2013.
13. Gleditsch et al. Armed conflict 1946–2001: A new dataset. *Journal of Peace Research*, 39(5), 2002.
14. Syntetos & Boylan. Accuracy of intermittent demand estimates. *International Journal of Forecasting*, 21(2), 2005.
15. Sharma, Patil & Rathi. Simulation-based optimization for spare parts. *Expert Systems with Applications*, 66, 2017.
16. Dalzochio et al. Predictive maintenance in the military domain. *ACM Computing Surveys*, 55(13s), 2023.

---

**Authors:** Thilak S · Aditya Raj · Bharat Raj Singal | Department of Mechanical Engineering | BITS Pilani, Pilani Campus \
**Supervisor:** Dr. Phaneendra Kiran Chaganti | Department of Mechanical Engineering | BITS Pilani, Hyderabad Campus \
**Venue:** LEAD 2025 Conference  \
**Contact:** [f20220771@pilani.bits-pilani.ac.in](mailto:f20220771@pilani.bits-pilani.ac.in)
