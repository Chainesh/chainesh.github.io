---
layout: page
title: Parameter Scaling in RL with Mixture of Experts
description: Soft-MoE DQN on Atari-100k
importance: 2
category: research
related_publications: false
---

A Soft-Mixture-of-Experts DQN with dynamic gating and top-k routing, which lets experts specialise while keeping their utilisation balanced.

On Atari-100k it converged about 15% faster than DQN, with about 35% lower variance in returns, at no extra compute cost.

[Code on GitHub](https://github.com/Chainesh/MOE-DQN-ATARI)
