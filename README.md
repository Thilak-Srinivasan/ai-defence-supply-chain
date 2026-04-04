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
| Barak | Missile Kits, Components | IAI, KRAS | State-owned reliance; regional instability; mitigated by JV | ![LOW–MODERATE](https://img.shields.io/badge/-LOW--MODERATE-yellow?style=flat-square) |
| K9 | Armament, Engine, Transmission | Hanwha, Hyundai WIA, STX | Multi-tier foreign dependency; mitigated by high local content | ![LOW](https://img.shields.io/badge/-LOW-brightgreen?style=flat-square) |

---

## AI Risk Scoring Model

### Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                        INPUT FEATURES                               │
│                                                                     │
│   hezbollah_mentions    iran_threat_level                           │
│   gaza_tension_index    domestic_politics_crisis                    │
└────────────────────────┬────────────────────────────────────────────┘
                         │
          ┌──────────────┴──────────────┐
          │                             │
          ▼                             ▼
┌──────────────────┐          ┌──────────────────────┐
│  RandomForest    │          │   LinearRegression   │
│  n_est=30        │          │   sklearn.linear_    │
│  max_depth=6     │          │   model              │
│  random_state=42 │          │                      │
└────────┬─────────┘          └──────────┬───────────┘
         │                               │
         ▼                               ▼
 conflict_risk (0–10)        eu_export_block_score (0–10)
```

### Geopolitical Risk Factor Weighting

| Risk Factor | Weight (%) | Data Source | Rationale |
|-------------|-----------|-------------|-----------|
| Last Conflict Year | **56.1** | COW MID v5.0 | Recency of conflict is the strongest predictor of recurrence risk |
| Militarized Disputes Count | **39.1** | COW MID v5.0 | Historical frequency of instability |
| Defence Cooperation | 2.6 | Bilateral agreements | Reduces risk via formal collaboration |
| Formal Alliance | 2.2 | COW Alliances dataset | Mutual support provides marginal protective effect |

### Synthetic Geopolitical Signal Set

| Signal | Value Range | Description |
|--------|-------------|-------------|
| `hezbollah_mentions` | 1–30 | Frequency of incidents in conflict reporting |
| `iran_threat_level` | 1–10 | Diplomatic tension and military posture indicators |
| `gaza_tension_index` | 1–10 | Recorded ceasefire violations, humanitarian alerts |
| `domestic_politics_crisis` | 1–3 | Internal stability metrics from global indices |

---

## Governing Equations & Model Details

### Random Forest Ensemble (Breiman, 2001)

The ensemble combines $T = 30$ decision trees, each trained on a bootstrap sample. Prediction is the average over all trees:

$$\hat{y} = \frac{1}{T} \sum_{t=1}^{T} h_t(\mathbf{x})$$

where $h_t(\mathbf{x})$ is the prediction of the $t$-th tree for input $\mathbf{x}$. Max depth = 6 is selected to balance bias-variance tradeoff.

### Feature Importance (Mean Decrease Impurity)

$$\text{Importance}(f) = \frac{1}{T} \sum_{t=1}^{T} \sum_{n \in \text{nodes splitting on } f} w_n \cdot \Delta I_n$$

where $w_n$ is the weighted sample fraction at node $n$ and $\Delta I_n$ is the impurity decrease.

### Linear Regression — EU Export Risk

$$\hat{y}_{\text{eu}} = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \beta_3 x_3 + \beta_4 x_4$$

where $x_1$ = hezbollah_mentions, $x_2$ = iran_threat_level, $x_3$ = gaza_tension_index, $x_4$ = domestic_politics_crisis.

### Risk Score Normalization

All outputs are normalized to a **0–10 scale**, where:

- **0–3**: Low risk — standard procurement pathway
- **3–5**: Low-to-moderate risk — monitor and prepare contingency
- **5–7**: Moderate risk — activate secondary sourcing
- **7–10**: High risk — trigger emergency alternative sourcing and stockpile activation

---

## Alternative Sourcing Recommendation Engine

### Semiconductor Components

| Country | Lead Time | Rationale |
|---------|-----------|-----------|
| Taiwan | 3 weeks | World leader in chip fabrication |
| South Korea | 4 weeks | Robust memory chip ecosystem |
| USA | 5 weeks | Defence-grade chip makers (Intel, etc.) |

### Drone Components

| Country | Lead Time | Rationale |
|---------|-----------|-----------|
| China | 5 weeks | Fast production and low cost |
| Turkey | 6 weeks | Bayraktar drone export expertise |
| USA | 7 weeks | High-end UAVs |

The engine accounts for geographic distance, bilateral trade relationships, regulatory approval processes, and verified alternative availability.

---

## Data Sources

| Dataset | Organization | Usage |
|---------|-------------|-------|
| Militarized Interstate Disputes (MID) v5.0 | Correlates of War (COW) Project | Historical conflict frequency and severity |
| Formal Alliances Dataset | COW Project | Alliance depth between India and supplier nations |
| UCDP/PRIO Armed Conflict Dataset | Uppsala Conflict Data Programme | Organized violence and sub-national instability |
| Georeferenced Event Dataset (GED) | UCDP | Spatial mapping of conflict events affecting supply regions |
| SIPRI Arms Transfer Database | Stockholm International Peace Research Institute | Global arms import/export trends |
| Company Annual Reports | Dassault, Boeing, Hanwha, L&T, TASL, Safran, et al. | JV structures, production capacities, strategic partnerships |
| Financial Intelligence Platforms | Fintel.io, Simply Wall St, Marketsmojo | Ownership structures of publicly traded defence contractors |

---

## Code Implementation

### Data Preparation

```python
import pandas as pd
import numpy as np
from sklearn.linear_model import LinearRegression
from sklearn.ensemble import RandomForestRegressor
import matplotlib.pyplot as plt

df = pd.DataFrame({
    "hezbollah_mentions":       [10, 5, 7, 20, 30, 25, 15, 12, 8, 28, ...],
    "iran_threat_level":        [6, 3, 4, 8, 9, 7, 5, 4, 2, 8, ...],
    "gaza_tension_index":       [3, 2, 4, 8, 9, 5, 3, 8, 7, 5, ...],
    "domestic_politics_crisis": [1, 0, 1, 2, 1, 1, 1, 2, 0, 1, ...],
    "conflict_risk":            [7.1, 6.2, 8.0, 5.0, 2.5, ...],
    "eu_export_block_score":    [5.8, 4.2, 6.4, 2.9, 1.0, ...]
})

X = df[["hezbollah_mentions", "iran_threat_level",
        "gaza_tension_index", "domestic_politics_crisis"]]
y_conflict = df["conflict_risk"]
y_eu       = df["eu_export_block_score"]
```

### Model Training (Appendix A.3)

```python
# Random Forest — conflict risk prediction
conflict_model = RandomForestRegressor(
    n_estimators=30,
    max_depth=6,
    random_state=42
)
conflict_model.fit(X, y_conflict)

# Linear Regression — EU export restriction likelihood
eu_model = LinearRegression()
eu_model.fit(X, y_eu)
```

### Inference & Prediction

```python
user_input = {
    "hezbollah_mentions":       23,
    "iran_threat_level":         8,
    "gaza_tension_index":        9,
    "domestic_politics_crisis":  1
}

X_user = pd.DataFrame([user_input])

predicted_conflict_risk = round(conflict_model.predict(X_user)[0], 2)
predicted_eu_risk       = round(eu_model.predict(X_user)[0], 2)

print("🔺 Conflict Risk Prediction:", predicted_conflict_risk, "/ 10")
print("🇪🇺 EU Arms Export Restriction Prediction:", predicted_eu_risk, "/ 10")
print("\n🔁 Recommended Alternate Suppliers:")
```

**Sample Output:**
```
🔺 Conflict Risk Prediction: 8.19 / 10
🇪🇺 EU Arms Export Restriction Prediction: 5.92 / 10

🔁 Recommended Alternate Suppliers:
```

### Alternative Sourcing Recommendation Engine

```python
def recommend_alternative_sources(product="semiconductors"):
    if product.lower() == "semiconductors":
        return [
            {"country": "Taiwan",      "lead_time": 3, "reason": "World leader in chip fabrication"},
            {"country": "South Korea", "lead_time": 4, "reason": "Robust memory chip ecosystem"},
            {"country": "USA",         "lead_time": 5, "reason": "Defence-grade chip makers like Intel"}
        ]
    elif product.lower() == "drones":
        return [
            {"country": "Turkey", "lead_time": 6, "reason": "Bayraktar drone export expertise"},
            {"country": "China",  "lead_time": 5, "reason": "Fast production and low cost"},
            {"country": "USA",    "lead_time": 7, "reason": "High-end UAVs"}
        ]
    else:
        return [{"country": "Unknown", "lead_time": -1, "reason": "Insufficient data"}]

for alt in recommend_alternative_sources("semiconductors"):
    print(f"- {alt['country']} → {alt['reason']} (Lead time: {alt['lead_time']} weeks)")
```

### Visualization

```python
plt.bar(
    ["Conflict Risk", "EU Export Risk"],
    [predicted_conflict_risk, predicted_eu_risk],
    color=["red", "blue"]
)
plt.title("Simulated Risk Forecast")
plt.ylim(0, 10)
plt.ylabel("Risk Score (0–10)")
plt.show()
```

---

## Repository Structure

```
ai-defence-supply-chain/
├── src/
│   ├── data_preparation.py          # Synthetic geopolitical dataset generation
│   ├── model_training.py            # RF + Linear Regression training pipeline
│   ├── risk_scoring.py              # Risk prediction and normalization (0–10 scale)
│   └── recommendation_engine.py     # Alternative sourcing recommendation logic
├── data/
│   └── synthetic_geopolitical.csv   # Sample synthetic signal dataset (non-classified)
├── appendix/
│   ├── A1_cow_dispute_durations.csv # Sample processed MID durations (Table A.1)
│   ├── A2_data_preparation.py       # Appendix A.2 — full data prep code
│   ├── A3_model_training.py         # Appendix A.3 — full model training code
│   └── A4_recommendations_viz.py    # Appendix A.4 — recommendations + visualization
└── README.md
```

---

## Strategic Implications

### Three Tiers of India's Defence Supply Chain Maturity

The mapping reveals three evolutionary tiers in India's industrial integration:

**Legacy Dependency** — S-400 Triumf
Single foreign supplier (Almaz-Antey), no meaningful technology transfer, complete operational vulnerability to geopolitical disruption. Real-world validation: Western sanctions on Russia directly caused multi-year delivery delays on a $5.5 billion committed programme.

**Transitional Integration** — Rafale Fighter Jet
Technology transfer agreements enable fuselage manufacturing through TASL — the first Rafale fuselage production outside France. Safran–India engine co-development for IMRH represents a shift from procurement to industrial participation.

**Advanced Partnership** — AH-64E Apache
Tata Boeing Aerospace (TBAL) in Hyderabad is the **exclusive global manufacturer** of AH-64 Apache fuselages for all Boeing customers worldwide. India has transitioned from end-consumer to a critical node in a major Western OEM's global supply chain — a fundamental shift in strategic role.

### Key Policy Insight

> Systems with deep technology transfer agreements (Apache fuselage, Barak joint development) demonstrate significantly higher supply chain resilience than legacy procurement models (S-400). Technology transfer depth should become the primary evaluation criterion for all future defence procurement decisions.

---

## Alternative Sourcing Recommendations

| System | Vulnerable Component | Current Supplier | Risk | Recommended Strategy | Alternative Suppliers |
|--------|---------------------|-----------------|------|---------------------|----------------------|
| S-400 | Radar, Missile Spares | Almaz-Antey (Russia) | ![HIGH](https://img.shields.io/badge/-HIGH-red?style=flat-square) | Domestic JV + diversified foreign sourcing | India–Russia JV; Western/Israeli alternatives (long-term) |
| Rafale | Engine Components, Avionics | Safran, Dassault, TASL | ![MODERATE](https://img.shields.io/badge/-MODERATE-orange?style=flat-square) | Deepen co-development; strategic stockpiling | HAL (India); Safran Helicopter Engines; Western partners |
| Apache | Engine, Radar, Targeting Spares | GE, Longbow LLC, Lockheed Martin | ![MODERATE](https://img.shields.io/badge/-MODERATE-orange?style=flat-square) | Diversified foreign sourcing; develop domestic MRO | Other US/European OEMs; domestic MRO expansion |
| Barak | Missile Kits, Components | Rafael (Israel) | ![LOW–MOD](https://img.shields.io/badge/-LOW--MOD-yellow?style=flat-square) | KRAS JV expansion; strategic stockpiling | KRAS expansion; DRDO-led domestication |
| K9 | Armament, Engine, Transmission | STX Engine, SNT Dynamics | ![LOW](https://img.shields.io/badge/-LOW-brightgreen?style=flat-square) | Expand domestic content beyond 60%; diversify | L&T (India); European/US suppliers |

---

## Future Research Directions

- **Real classified data integration** — transition from synthetic geopolitical signals to actual telemetry, maintenance logs, and operational data through secure collaboration with Indian Army stakeholders under a validated data-sharing framework
- **Broader platform coverage** — extend multi-tier mapping to naval systems (Scorpene submarines, INS Vikrant carrier air wing) and DRDO indigenous programmes (Tejas, Arjun Mk2, Pinaka)
- **NLP-enhanced risk monitoring** — integrate real-time news sentiment analysis (defence journals, diplomatic communiqués, sanctions announcements) into the continuous risk feed
- **Spare demand surge modelling** — link geopolitical risk scores to probabilistic spare demand distributions to enable stockpile optimization under conflict scenarios
- **Digital twin integration** — couple the AI risk layer with equipment digital twins for real-time failure prediction calibrated against both operational tempo and supply chain risk state
- **Multi-objective optimisation** — simultaneously minimise: (i) stockpile holding cost, (ii) risk of operational unavailability, (iii) foreign dependency index — subject to budget and lead-time constraints

---

## Novel Contributions

1. **First structured multi-tier mapping** of India's five critical defence platforms (S-400, Rafale, Apache, Barak, K9) using OSINT — extending beyond Tier 1 OEMs to expose hidden Tier 2/3 vulnerability nodes
2. **Geopolitical AI risk engine** — objective, data-driven quantification of supplier country risk using COW and UCDP structured datasets, replacing subjective expert judgement
3. **Predictive validation** — model predicted elevated Russian supplier risk months ahead of S-400 delivery disruptions, confirming early warning operational value
4. **Ownership structure risk taxonomy** — first classification of defence supplier risk by state-owned enterprise vs. publicly traded vs. mixed ownership, revealing distinct risk profiles for each
5. **Technology transfer as resilience metric** — demonstrates that technology transfer depth (not procurement volume) is the primary determinant of long-term supply chain resilience — directly actionable for India's defence acquisition policy
6. **Automated alternative sourcing engine** — recommendation system that factors lead time, bilateral trade relationships, regulatory approval, and geographic risk into ranked alternative sourcing options

---

## References

1. Stanton, I., Munir, K., Ikram, A., and El-Bakry, M. Predictive maintenance analytics and implementation for aircraft: Challenges and opportunities. *Systems Engineering*, 26(1), e21651, 2023.
2. Ochando, F. J., et al. Data acquisition for condition monitoring in tactical vehicles: On-board computer development. *Sensors*, 23(12), 5645, 2023.
3. Simion, D., et al. AI-driven predictive maintenance in modern maritime transport. *Applied Sciences*, 14(20), 9439, 2024.
4. Kalafatelis, A. S., et al. Towards predictive maintenance in the maritime industry. *Journal of Marine Science and Engineering*, 13(3), 425, 2025.
5. Choi, B. and Suh, J. H. Forecasting spare parts demand of military aircraft. *Sustainability*, 12(15), 6045, 2020.
6. Kim, J.-D. and Kim, T.-H. Demand forecasting of spare parts using artificial intelligence. *Mathematics*, 11(3), 501, 2023.
7. Kim, J.-D., Hwang, J.-H., and Doh, H.-H. A predictive model with data scaling for spare parts demand in military logistics. *Defence Science Journal*, 73(6), 666–674, 2023.
8. Sharma, M., Ansar, A., and Parkhe, P. Inventory woes and logistic bottlenecks in Indian defence SCM. *Defense and Security Studies*, 6(1), 2025.
9. Singh, A. P. Atmanirbharta Bharat: India's self-reliance and supply chain resilience. *Journal of Defence Studies*, 18(4), 374–376, 2024.
10. Elvemo, L. Supply chain resilience in military operations. *Scandinavian Journal of Military Studies*, 8(1), 178–199, 2025.
11. Singer, J. D. and Bremer, S. Interstate war: An event-data approach. *Journal of Conflict Resolution*, 32(2), 313–332, 1988.
12. Sundberg, R. and Melander, E. Introducing the UCDP Georeferenced Event Dataset (GED). *Journal of Peace Research*, 50(4), 523–532, 2013.
13. Gleditsch, N. P., et al. Armed conflict 1946–2001: A new dataset. *Journal of Peace Research*, 39(5), 615–637, 2002.
14. Syntetos, A. A. and Boylan, J. E. The accuracy of intermittent demand estimates. *International Journal of Forecasting*, 21(2), 303–314, 2005.
15. Sharma, P., Patil, M. S., and Rathi, V. Simulation-based optimization for spare parts forecasting and selective maintenance. *Expert Systems with Applications*, 66, 117–132, 2017.
16. Dalzochio, J., et al. Predictive maintenance in the military domain: A systematic review. *ACM Computing Surveys*, 55(13s), Article 267, 2023.

---

**Authors:** Thilak S · Aditya Raj · Bharat Raj Singal | Department of Mechanical Engineering, BITS Pilani  
**Supervisor:** Dr. Phaneendra Kiran Chaganti | BITS Pilani, Hyderabad Campus  
**Venue:** LEAD 2025 Conference  
**Contact:** [f20220771@pilani.bits-pilani.ac.in](mailto:f20220771@pilani.bits-pilani.ac.in)
