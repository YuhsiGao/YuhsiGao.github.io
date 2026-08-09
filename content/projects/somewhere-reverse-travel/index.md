---
title: Somewhere · Reverse Travel Agent
summary: A consumer AI travel product that turns a feeling into a destination.
date: 2026-08-01
weight: 2
---

**Somewhere / 去处** is a consumer AI travel prototype built around a simple idea: users do not need to know where they want to go before they start. They can describe a feeling, a pace, or a kind of life they want to enter, and the product helps translate that into a destination and an executable short trip.

## Product experience

- Understands natural-language descriptions of mood, weather, pace, social density, and travel constraints.
- Shows the Agent's exploration process without exposing private chain-of-thought.
- Compares three destinations with different roles, matching reasons, and trade-offs.
- Lets users confirm hard constraints such as region, duration, budget, and transport before filtering results.
- Produces a three-day itinerary with time feasibility, map references, weather checks, route evidence, and explicit unverified states.

## Product thinking

The product does not treat an LLM as a travel-guide generator. The model is responsible for understanding and structuring the user's intent; candidates, constraints, ranking, and evidence are handled by structured data and rule layers. This keeps the experience explainable and makes it possible to distinguish generated suggestions from information that still needs verification.

## Technical implementation

- React, TypeScript, Vite, and native CSS for the responsive C-end experience.
- TokenHub through a server-side proxy for structured travel-intent parsing, with a local demo fallback.
- Agent workflow covering vibe interpretation, destination exploration, reality checking, and itinerary editing.
- MapLibre GL JS and OpenStreetMap for on-demand interactive maps and route references.
- User-triggered weather, route, nearby-place, and POI-reference checks through controlled BFF endpoints.
- Local-only preference, favorites, media preview, sharing, and decision-package export flows.

The project explores how an AI product can move from an ambiguous emotional request toward a decision that is understandable, evidence-aware, and useful in the real world.
