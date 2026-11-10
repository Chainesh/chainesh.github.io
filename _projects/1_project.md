---
layout: page
title: Context Robustness in Time-Series Foundation Models
description: which part of the input history TimesFM, TTM and Chronos actually use
importance: 1
category: research
related_publications: false
---

A context contamination framework showing that TimesFM, TTM and Chronos rely mainly on the last 10% of their input history.

Building on this, I split each series into trend, seasonal and residual parts and built an ensemble that gives each part to the model that forecasts it best. The ensemble cut forecast error by about 3% over the best single model on low-seasonality data, and matched it on strongly seasonal data.

[Code on GitHub](https://github.com/Chainesh/context_contamination)
