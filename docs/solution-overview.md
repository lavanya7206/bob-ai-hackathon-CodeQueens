# Solution Overview

## What We Built

ChainGuard AI is a supply-chain disruption and fleet intelligence solution. It helps logistics operators identify affected shipments, prioritize risks, find alternative routes, match available vehicles, and detect cold-chain temperature risks.It provides clear and explainable recommendations instead of making teams handle every disruption manually.

## How It Works

1. A road, route, or facility disruption is simulated.
2. ChainGuard identifies the shipments affected by the disruption.
3. The system calculates a risk score for each affected shipment.
4. Alternative routes and available fleet vehicles are evaluated.
5. The system recommends a suitable route and vehicle.
6. Temperature data is checked to identify cold-chain risks.
7. The operator receives priorities, recommendations, alerts, and explanations.

**Flow:** Detect → Prioritize → Recommend → Act

## Architecture Diagram

```text
[Logistics Operator]
        ↓
[Dashboard / Demo Mode / AI Assistant]
        ↓
[Data Layer]
Shipments • Fleet • Routes • IoT Readings
        ↓
[Decision Engine]
Risk Scoring • Route Selection
Fleet Matching • Temperature Rules
        ↓
[Action Layer]
Priorities • Recommendations
Alerts • Explanations

## Key Design Decisions

Rule-based risk scoring – Provides simple and explainable shipment risk decisions.
Route optimization – Recommends alternate routes when a disruption occurs.
Fleet matching – Matches affected shipments with suitable idle vehicles.
Cold-chain monitoring – Detects temperature excursions and identifies their severity.
Mock operational data – Keeps the prototype self-contained and easy to demonstrate.
Explainable recommendations – Shows the reason behind priorities and suggested actions.

## IBM Technologies Used

IBM Bob: Used as an AI development partner for project planning, architecture, code generation, debugging, UI improvements, and documentation.
watsonx.ai: Planned integration path for an LLM-powered logistics copilot that can answer natural-language operational queries using shipment, fleet, and sensor context.
