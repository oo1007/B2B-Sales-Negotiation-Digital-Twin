# B2B-Sales-Negotiation-Digital-Twin
# B2B Sales Negotiation Digital Twin

An interactive simulation dashboard for exploring how proposal terms, committee dynamics, and LLM-assisted diagnostics shape B2B sales negotiation outcomes.

## Live Demo
🔗 [View the website](https://oo1007.github.io/B2B-Sales-Negotiation-Digital-Twin/)

---

## Project Overview

This project presents a **B2B Sales Negotiation Digital Twin** designed to simulate complex enterprise deal-making processes.  
It transforms the "black box" of multi-stakeholder B2B negotiation into a more structured and observable system.

The dashboard allows users to:

- Adjust proposal parameters through interactive sliders
- Observe changes in dynamic negotiation state variables
- Explore the internal logic of both **buyer** and **seller committees**
- View LLM-assisted outputs such as risk checks, round summaries, buyer deliberation, and final diagnostic reports
- Understand how committee dynamics, redlines, concessions, and political influence affect negotiation outcomes

---

## Key Features

### 1. Proposal Parameter Controls
Users can modify important deal terms through sliders, including:

- AVC
- Contract Duration
- Payment Terms
- Liability Cap
- Implementation Speed
- Scope Rigidity

These variables represent the negotiable components of a proposal and directly influence committee evaluation and simulation outcomes.

### 2. Dynamic Negotiation State
The dashboard tracks key variables that evolve during the simulation, such as:

- Current Round
- Champion Influence
- Institutional Trust
- Seller Margin Remaining
- No-Decision Pressure

This helps visualize how negotiation pressure and internal alignment change over time.

### 3. Buyer & Seller Committee Views
The dashboard includes clickable entry points into the internal logic of both committees.

#### Seller Internal Logic
The seller-side model contains two major parts:

- **Internal Alignment**: uses LLM summarization to synthesize buyer feedback and identify the current **concession level** and **concession focus**
- **Upgrade Proposal**: updates proposal-related parameters based on the identified concession focus

#### Buyer Internal Logic
The buyer-side model contains multiple components:

- **Initial Compute Utility**: calculates initial utility based on each buyer’s role
- **Utility Compute Per Round**: updates utility after each discussion round
- **Buyer Discussion**: uses an LLM to simulate internal discussion among buyers, generating dialogue records and updated utilities
- **Divergence Check**: measures alignment or disagreement across committee members
- **Political Intervention**: applies influence logic based on whether `champion_clout_current > 0` and whether the actor is a business buyer

### 4. LLM-Assisted Outputs
The right-side output panel presents four dimensions of model-generated narrative interpretation:

- **Live Risk Check**
- **Round Summary**
- **Buyer Deliberation**
- **Final Diagnostic Report**

This makes the simulation more interpretable and presentation-friendly by combining structured state updates with natural-language insights.

---

## Why This Project

B2B negotiations often involve multiple stakeholders with different priorities, constraints, and decision rules.  
This project aims to make those interactions more transparent by combining:

- simulation thinking
- committee-based decision logic
- dynamic state tracking
- LLM-generated narrative outputs

The result is a prototype that can be used for **demonstration, explanation, and scenario exploration**.

---

## Tech Stack

- **HTML**
- **CSS**
- **JavaScript**
- **GitHub Pages** for deployment

---

## Project Structure

```text
index.html      # Main dashboard page
README.md       # Project documentation
