---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

## High-Frequency Stock Return Prediction with Sector Lead-Lag Signals

**Team Leader, Guotai Haitong Quantitative Modeling Competition**  
Mar. 2026 - Apr. 2026

This project studied whether intra-sector information diffusion can improve short-horizon return prediction from tick-level data. Given five stocks from the same concept sector, I led the construction of a model to predict the future 5-minute return of the target stock.

The core idea was to separate two information channels. The **E-stream** modeled the target stock's own order-book and microstructure state, while the **Board-stream** modeled sector-level spillover signals from peer stocks. I designed dynamic leader-stock identification, lagged sector-shock features, and relative-deviation signals to capture lead-lag effects inside the sector.

The final model used regularized Ridge Regression and a fusion layer, with time-series validation and bootstrap robustness checks. It achieved **IC = 0.1994** for 5-minute return prediction in the competition setting.

## Regime-routed Transformer for High-Frequency Return Prediction

**Lead Researcher**  
May 2026

This project focused on minute-level return prediction for 30 anonymous high-volatility assets. The data showed strong regime and market-structure heterogeneity, so I first classified the datasets into futures-like, crypto-like, and stock-like markets using trading-hour structure, extreme-window duration, and tail enrichment.

I built a causal feature pipeline covering momentum, volatility, liquidity, peer-anchor, market-specific, and state-quality signals. The model used robust scaling, tail-aware target transformations, and a normal/extreme dual-expert Transformer with routing logic. LightGBM was also used where tree-based models were more stable for small or stock-like samples.

In external validation on **10.6M rows**, the final conservative route used normal experts for crypto/futures and LightGBM for stock-like datasets, reaching **Ret5 IC 0.0104**, **Ret60 IC 0.0174**, and **mean IC 0.0139**. A key conclusion was that aggressive extreme routing can hurt when the external distribution is mostly normal-like.

## Domestic Macro Asset Dynamic Allocation Model

**Independent Lead**  
Jul. 2023 - Jul. 2024

This project began as an independent research study on adapting Markowitz mean-variance optimization to domestic household asset allocation. I studied portfolio theory, consulted finance professionals, collected historical domestic asset data, and implemented rolling backtests in Python.

The model combined return-probability estimation, EWMA smoothing, signal remapping, volatility scaling, and EWMA covariance forecasting. To reduce the computational burden of rolling optimization, I derived analytical gradients and Jacobian matrices for the optimization procedure.

Across a 2006-2023 backtest, the model achieved a **Return/Risk ratio of 1.0** versus **0.79** for a fixed-income benchmark. The optimized implementation reduced a 17-year rolling backtest from nearly 1 hour to 90 seconds, about a **40x speedup**.

## TDA-based Style Rotation and Crowding Analysis

**Buy-side Quantitative Research Internship**  
Jun. 2025 - Aug. 2025

I worked on a timing strategy for small-cap versus large-cap style rotation using macro indicators and micro-level crowding signals. To capture structural changes in market crowding, I introduced Topological Data Analysis and Persistent Homology as a way to detect changes in the shape of crowding conditions.

The resulting framework used crowding inflections as style-rotation signals and achieved a backtest **Sharpe Ratio above 1.0**. This project strengthened my interest in translating abstract mathematical tools into practical market-state indicators.

## Fixed-Income Relative Value and Bond Pair Trading

**Fixed-Income Quant Strategy Internship**  
Jan. 2026 - Present

I researched bond pair trading ideas based on yield-spread relationships, relative value, and mean-reversion logic. The work strengthened my understanding of fixed-income market structure, rates trading, interest-rate risk, and strategy validation workflows.

This experience is still ongoing, so I keep public descriptions high-level and avoid disclosing internal strategy details.
