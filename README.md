# Okey Rizikolu Sistem — Game Probability & Risk Engine Case Study

> **Notice:** This repository is an **Architectural Case Study & Engineering Showcase**. Proprietary mathematical algorithms and internal scoring engines remain private.

---

## 🏛️ Executive Summary

**Okey Rizikolu Sistem** is an analytical math and decision-support engine engineered to calculate real-time hand probabilities, tile distribution risks, and mathematically optimal tile discard choices in strategic tile-based games (101 Okey).

---

## ⚡ Key Engineering & Mathematical Achievements

- **Combinatorial Hand Evaluator:** Evaluates all possible tile permutations in < 15 milliseconds, calculating exact turns to completion (distance to meld).
- **Discard Risk Matrix:** Quantifies opponent tile intake probability based on remaining unseen tile pools and discard history.
- **Monte Carlo Strategy Simulator:** Simulates 10,000 game branch completions per turn to determine high-EV (expected value) plays.

---

## 📐 Architecture Overview

```
   ┌────────────────────────────────────────────────────────┐
   │               Board State Input / Vision               │
   └───────────────────────────┬────────────────────────────┘
                               │
                               ▼
   ┌────────────────────────────────────────────────────────┐
   │        Combinatorial Tile Permutation Engine           │
   └───────────────────────────┬────────────────────────────┘
                               │
             ┌─────────────────┴─────────────────┐
             ▼                                   ▼
  ┌──────────────────────┐            ┌─────────────────────┐
  │ Hand Completion Dist │            │ Tile Discard Risk   │
  │ (Distance to Meld)   │            │ Probability Matrix  │
  └──────────┬───────────┘            └──────────┬──────────┘
             │                                   │
             └─────────────────┬─────────────────┘
                               ▼
   ┌────────────────────────────────────────────────────────┐
   │     Optimal Discard Recommendation & Risk Score        │
   └────────────────────────────────────────────────────────┘
```

---

## 📊 Performance Benchmarks

| Metric | Benchmark Value |
|--------|-----------------|
| **Permutation Evaluation Time** | < 12 ms |
| **Monte Carlo Iterations / Turn** | 10,000 Simulations |
| **Hand Completion Accuracy** | 99.8% |

---
*Architected and engineered by **Enes Teke (tekedev)**.*
