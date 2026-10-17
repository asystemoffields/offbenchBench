---
slug: openclimatefix-quartz-nwp-units
title: Live NWP inputs fed to the solar model in the wrong units
url: https://github.com/openclimatefix/open-source-quartz-solar-forecast/issues/375
field: solar PV forecasting
status: submitted
---

# Worked example: Open Climate Fix, Quartz Solar Forecast

This is a real contribution, written up to show the protocol end to end at the standard tier. Use it to calibrate what "good" looks like for a software change. For what the high-stakes tier demands, see `erdos-ai-precedents.md`.

**Project:** [Open Climate Fix](https://github.com/openclimatefix) is a non-profit that builds open solar and wind forecasting. `open-source-quartz-solar-forecast` predicts output for individual PV sites from numerical weather prediction (NWP) data fetched from Open-Meteo.

## How it went through each phase

**Discover.** The README itself flagged that one input (`dlwrf`) needed someone to "confirm it is correct". That is a maintainer asking for help in the docs instead of a label.

**Evaluate.** Standard tier: a wrong forecast costs users, but the fix lands in a reviewed codebase and nobody is relying on the claim until it is merged. The scores were high on every dimension that matters most:

- **Stakes:** the flagged input feeds every forecast the package makes.
- **Verifiability:** the fitted model stores its training feature ranges, so the expected units can be read straight off it, and forecasts can be backtested against public PV data.
- **Traction:** the mismatch can be reproduced directly from the public model and data. There is no private data or special hardware.

**Solve, first finding.** Checking the one flagged variable turned up a bigger problem. Three other inputs were also in the wrong units: temperature in °C instead of K, wind in km/h instead of m/s, and precipitation per hour instead of per second. `dlwrf` was being fed *shortwave* radiation instead of longwave. The evidence came from the model's own histogram bin edges, a primary source, rather than from documentation. It was **reported as an issue first** ([#375](https://github.com/openclimatefix/open-source-quartz-solar-forecast/issues/375)). The issue included:

- a table of mismatches
- the code that reproduces them
- an impact estimate: a backtest over 8 sites and 26 forecast runs, with a paired bootstrap 95% CI
- caveats, such as using national data as a proxy for true site output
- three options for the input with no direct equivalent, and an offer to open a PR

**Maintainer response.** A maintainer asked for a PR and chose an option: "I'd probably go for a) first, then see what b) does." That steered the PR toward what the project wanted.

**Solve, the fix.** [PR #376](https://github.com/openclimatefix/open-source-quartz-solar-forecast/pull/376) made the changes:

- It converts the units and estimates longwave radiation with a published method (Brutsaert 1975).
- It maps variables by name instead of by position, so a reordering can't silently shift features again.
- Its tests fail when any of the conversions is removed.

The PR evaluated both options the maintainer named, and showed the recommended one was better: daytime error fell from 6.32% to 4.31%, with a CI that excludes zero. It also checked the estimate against an independent dataset (NASA POWER) and reported where the estimate runs high.

**Side finding.** A dependency incompatibility that also broke `main` was found during testing. It was filed as its own issue ([#377](https://github.com/openclimatefix/open-source-quartz-solar-forecast/issues/377)) with a version matrix, not folded into the PR.

**Contribute.** Every public post disclosed AI assistance in one line.

## Lessons

- Look past the flagged symptom. The flagged variable led to the real bug, which was larger.
- Use the artifact itself as evidence. The fitted model's stored ranges were more reliable than the docs.
- Start with an issue that offers options, so the maintainer chooses the direction before you write the code.
- Keep each contribution in scope, and send side findings to their own threads.
