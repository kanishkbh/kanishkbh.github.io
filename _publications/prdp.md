---
title: "PRDP: Progressively Refined Differentiable Physics"
collection: publications
category: conferences
permalink: /publication/prdp
redirect_to: https://kanishkbh.github.io/prdp-paper/
# excerpt: 'This paper is about a famous math equation, $$E=mc^2$$'
date: April 2025
venue: 'The Thirteenth International Conference on Learning Representations, {ICLR} 2025, Singapore, April 24-28, 2025'
paperurl: 'https://arxiv.org/pdf/2502.19611'
# citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
---

The physics solvers employed for neural network training are primarily iterative, and hence, differentiating through them introduces a severe computational burden as iterations grow large. Inspired by works in bilevel optimization, we show that full accuracy of the network is achievable through physics significantly coarser than fully converged solvers. We propose Progressively Refined Differentiable Physics (PRDP), an approach that identifies the level of physics refinement sufficient for full training accuracy. By beginning with coarse physics, adaptively refining it during training, and stopping refinement at the level adequate for training, it enables significant compute savings without sacrificing network accuracy. Our focus is on differentiating iterative linear solvers for sparsely discretized differential operators, which are fundamental to scientific computing. PRDP is applicable to both unrolled and implicit differentiation. We validate its performance on a variety of learning scenarios involving differentiable physics solvers such as inverse problems, autoregressive neural emulators, and correction-based neural-hybrid solvers. In the challenging example of emulating the Navier-Stokes equations, we reduce training time by 62%.

![PRDP Teaser Image](/images/prdp_teaser.png)