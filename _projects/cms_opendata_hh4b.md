---
layout: page
title: CMS Open Data HH → 4b Multijet & Mixed Datasets
description: Reconstructed collision, hemisphere-mixed synthetic data, and simulations in Parquet format for di-Higgs multijet background modelling.
date: 2026-11-05
importance: 1
category: work
redirect: https://huggingface.co/datasets/alefisico/LHC_HH4b_mixeddata
---

This dataset contains flat tabular (Apache Parquet) collision data and simulated physics processes released by the **CMS Collaboration** on the **CERN Open Data Portal** ([Record cms-93965](https://opendata.cern.ch/record/cms-93965)) and hosted on **Hugging Face** ([alefisico/LHC_HH4b_mixeddata](https://huggingface.co/datasets/alefisico/LHC_HH4b_mixeddata)).

It is prepared for machine-learning-based background modelling, density ratio estimation, and domain-adaptation reweighting in multijet searches for di-Higgs production in the four-bottom-quark final state ($pp \to HH \to (b\bar{b})(b\bar{b})$).

### Key Features

- **Format**: Flat tabular Apache Parquet files partitioned by process and tag categories.
- **Collision Data**: CMS Run 2 ($13\text{ TeV}$) multijet collision data in the 3b source domain.
- **Synthetic Mixed Data**: Signal-free 4b pseudo-data generated via hemisphere mixing for authentic domain-adaptation benchmarks and unblinded evaluation.
- **Simulations**: Detailed Monte Carlo samples for $t\bar{t}$ and resonant backgrounds ($ZH$, $ZZ$, and $HH$ signal).
- **Interactive Quickstart**: End-to-end tutorial notebook runnable directly in Google Colab without downloading the full dataset locally.

### Links & DOI

- **Hugging Face Dataset**: [https://huggingface.co/datasets/alefisico/LHC_HH4b_mixeddata](https://huggingface.co/datasets/alefisico/LHC_HH4b_mixeddata)
- **CERN Open Data Record**: [https://opendata.cern.ch/record/cms-93965](https://opendata.cern.ch/record/cms-93965)
- **DOI**: [10.7483/OPENDATA.CMS.WWHU.D4ON](https://doi.org/10.7483/OPENDATA.CMS.WWHU.D4ON)
