# Eiger count rate and dose: interactive demo

Interactive notebook from the Diamond Light Source I04 MX refresher training (case study "Precision at High Flux").

Move the transmission slider and switch crystal type to see:

- **Count rate (left).** At 100 % transmission, a strongly diffracting crystal pushes the brightest detector pixels past the Dectris trusted limit. Counts are lost, and merging statistics don't reveal it.
- **Dose (right).** Lowering transmission and increasing total exposure in proportion delivers **the same total dose**: same data, collected more slowly, with every photon counted.

## Run it in your browser (no installation)

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/aragaod/eiger-countrate-dose-demo/HEAD?labpath=Interactive_count_rate_graph_v2.ipynb)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aragaod/eiger-countrate-dose-demo/blob/main/Interactive_count_rate_graph_v2.ipynb)

Then choose **Run → Run All Cells** (Binder) or **Runtime → Run all** (Colab).

## Run it locally

```bash
pip install -r requirements.txt
jupyter lab Interactive_count_rate_graph_v2.ipynb
```

## What the numbers are

- **Detector curve:** paralyzable dead-time model *m = n·exp(−n·τ)*, fitted to the EIGER count-rate curve at 12.4 keV published by DECTRIS. The flux scale is illustrative.
- **Dose:** 10 MGy at 100 % transmission takes 16 s on I04 at 13 keV with the default beam (RADDOSE-3D, about 0.62 MGy/s). At any other transmission T, the total exposure for the same dose is 16 s / T.
- The crystal types are illustrative strengths, not measured values.

At I04, ask beamline staff to check your own strong crystals with a short 15° screen before a full collection.
