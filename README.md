# assertion-router

Four-mode confidence routing for AI systems: **ASSERT**, **PROBABILISTIC**, **INVESTIGATIVE**, or **REFUSE**, selected by the epistemic certainty behind the answer, not by the content of the answer itself.

## The problem

Most systems pick one register and stick to it — either they answer everything with the same flat confidence, or they hedge everything the same way regardless of how sure they actually are. Neither is honest. A system that's 95% certain and a system that's 40% certain shouldn't sound the same.

## What it does

assertion-router sits between a reasoning pipeline's internal confidence signal and its final output, and picks the mode that matches:

- **ASSERT** — state it directly, no qualification
- **PROBABILISTIC** — state it with calibrated uncertainty language
- **INVESTIGATIVE** — surface the question rather than an answer; the certainty isn't there yet
- **REFUSE** — decline, when the honest answer is "this can't be determined reliably"

The routing decision is separate from content generation. It's a layer, not a rewrite.

## Part of a family

assertion-router is one of several reasoning-layer engines built around the same problem space — routing, scoring, and gating AI output on epistemic grounds rather than surface plausibility. See [davidkirsch.me/builds](https://davidkirsch.me/builds) for how they fit together.
