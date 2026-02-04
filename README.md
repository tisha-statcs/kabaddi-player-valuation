# Modeling the Economic Value of a Kabaddi Player Over Time

This repository contains my response to **Problem 3: How Valuable Is a Player, Really?** that was proposed as part of an analytical exercise for the WKCL ecosystem.

The purpose of this project is to develop a quantitative model for measuring the value of a Kabaddi player at different times, acknowledging that a player generates value beyond on-field statistics. Specifically, the model will account for:

- the on-field performance,
- the engagement with fans and the commercial value generated,
- the uncertainty related to the availability and injuries to the player,
- and the change over time due to the form cycle, the workload of the player, and the attention dynamics.

The framework for this approach is called **Total Economic Value (TEV)**, and it considers a player as a dynamic economic asset rather than a static performer.

---

## Background for Problem

Players in Kabaddi generate value for their teams not only through their raid points or the outcome of a game, but they also generate additional value through:

- their consistency in each match,
- their ability to attract a large number of viewers and to capture the attention of fans,
- their commercial value created through the sale of merchandise and through engagement,
- and their physical condition and availability during a long season.

Therefore, any realistic valuation model for a player must:

- take into consideration the evolution of the player's value over time and
- account for the uncertainty, with regards to the risk of injury.

---

## Overview of Solution

Player value is defined by the TEV model through a decomposition of the value into three components, which include:

- on field performance value,
- commercial (fan engagement) value,
- digital asset value,

which are then combined and discounted by a probabilistic risk factor to take into consideration the uncertainty.

---

## Documentation

More details about the model, the equations and the variables used in the model can be found in the following document:

 **Problem_3_Player_Value.md**
