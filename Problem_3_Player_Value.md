# Problem 3: Modeling the Economic Value of a Kabaddi Player Over Time

This document presents my solution to **Problem 3: How Valuable Is a Player, Really?**, which asks how to model the economic value of a Kabaddi player over time while accounting for **uncertainty** and **change**.

To model the economic value of a Kabaddi player over time, I propose a quantitative framework called Total Economic Value (TEV).
The main idea is to treat a player as a **dynamic economic asset** whose value changes with on field performance, fan engagement, and availability, rather than just match statistics.

**The model explicitly accounts for change over time through performance trajectories and for uncertainty through injury related risk.**
---

In Kabaddi, a player contributes value in multiple ways:

- through on field performance such as raid output and consistency,
- through their ability to attract fan attention and viewership,
- through commercial outcomes such as merchandise demand,
- and through their availability, which is affected by workload and injury risk.

A valuation framework must therefore:
- evolve over time,
- go beyond single match statistics,
- and account for uncertainty.

---

## Modeling Framework: Total Economic Value (TEV)

To capture these aspects, I define a framework called **Total Economic Value (TEV)**.

At time t, the economic value of a player is defined as:

![Total Economic Value Equation](equations/tev_equation.jpg)

where:
- V_P(t) is the **on field performance value**,  
- V_C(t) is the **commercial value driven by fan engagement**,  
- V_D(t) is the **digital asset value**,  
- P_{Risk}(t) is the **probability of value loss** due to injury or decline.

The multiplicative risk term ensures that uncertainty directly reduces expected value.

---

## On Field Performance Value V_P(t)

On field performance value measures how much a player contributes during raids and how consistently they perform across matches.

Rather than treating performance as fixed, the model allows it to **change over time** using a life cycle adjustment.

![On-Field Performance Value](equations/performance_equation.jpg)


### Performance Variables

- **RP (Raid Points):** Total raid points scored by the player.  
- **SRR (Successful Raid Rate):** Proportion of raids that result in points.  
- **ST (Super Tens):** Number of matches with 10 or more raid points.  
- **ω₁, ω₂, ω₃:** Weights reflecting the relative importance of each metric.

### Change Over Time

The multiplier φ(t, B, R) allows on field performance value to vary over time instead of remaining constant.

- **B (Biological / workload state):** Short term recovery and fatigue state between matches.
- **R (Latent resilience):** Long term availability pattern based on past match participation.

The variable B changes frequently with match load and recovery, while R changes slowly over time.  
Together, they allow the model to account for form cycles, performance peaks, and gradual performance decline over a season or career.

---

## Commercial Value and Fan Attention V_C(t)

Commercial value reflects a player’s ability to generate revenue through **fan engagement and viewership**, not just popularity.

![Commercial Value Equation](equations/commercial_equation.jpg)


### Commercial Variables

- **E_{Rate}:** Digital engagement rate (likes, shares, interactions).  
- **M_{Sales}:** Merchandise demand associated with the player.  
- **V_{Corr}:** Statistical relationship between engagement and match viewership.  
- **β₁ β₂ β₃:** Weights capturing commercial importance.

### Attention Cycles

- **α(t):** An attention factor that models the rise and fall of fan interest across a season.

This reflects the idea that **fan attention is finite** and responds to performance streaks and match narratives.

---

## Digital Asset Value V_D(t)

Digital asset value represents economic value created through:
- proprietary digital rights,
- digital collectibles,
- performance-linked digital initiatives.

This component allows the model to incorporate modern revenue channels that evolve alongside fan engagement.

---

## Modeling Uncertainty: Injury and Availability Risk P_{Risk}(t)

Uncertainty in player value mainly arises from **injury risk**, which affects both on field contribution and commercial outcomes.

Injury risk is modeled using logistic regression:

![Injury and Availability Risk](equations/risk_equation.jpg)


### Risk Variables

- **S:** Training stimulus and cumulative workload.  
- **T:** Technique related biomechanical stress indicators.  
- **B:** Short term recovery and fatigue state between matches.  
- **R:** Long term availability pattern based on past match participation.

A higher estimated risk reduces the risk adjusted economic value.

---

## Interpretation of the Model

- **Change:**  
  Captured through φ(t) (performance trajectory) and α(t) (attention cycles).

- **Uncertainty:**  
  Captured through P_{Risk}(t) which directly discounts value.

- **Economic Meaning:**  
  A player who performs well, remains available and sustains fan attention will have higher TEV than a player with similar skill but higher risk or declining engagement.

---

This TEV framework treats a Kabaddi player as a changing economic asset rather than a fixed performer.
By combining on field performance, fan engagement, and risk into a single structure, it provides a clear way to understand how player value changes over time.

---

