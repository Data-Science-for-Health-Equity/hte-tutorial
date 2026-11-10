# What Works for Whom: Assessing Heterogeneous Treatment Effects

**DSxHE Data Diversity × Statistical Methods Tutorial, in collaboration with Cancer Research UK**
**Presenter:** Dr Carly Brantner, Duke University · **Session:** 10 September 2026

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Data-Science-for-Health-Equity/hte-tutorial/blob/main/hte_tutorial_notebook.ipynb)

Averages can mislead. A treatment can look effective overall while doing little for, or even harming, large parts of the population it is meant to help. Heterogeneous treatment effects (HTE) describe how a treatment's benefit differs from person to person rather than only its average across a trial population. Knowing who benefits, and who doesn't, is central to delivering more equitable care.

This 90-minute interactive tutorial covers detecting, estimating and interpreting that variation. It live-codes in R on a simulated dataset modelled on a trial comparing treatments for depression, moving from traditional approaches (interaction terms, stratified analysis) to causal forests.

📺 **Recording, slides and event recap:** [DSxHE blog post](https://www.datascienceforhealthequity.com/post/dsxhe-data-diversity-x-stasitical-methods-tutorial-what-works-for-whom-assessing-heterogeneous)

## Getting started

1. Click **Open in Colab** above and sign in to a Google account.
2. Choose **File → Save a copy in Drive** and work in your copy.
3. The notebook uses the **R** runtime. If Colab opens it in Python, use **Runtime → Change runtime type → R**.
4. Run the cells top to bottom. The package-install cell can take a few minutes the first time.

You can also download the notebook and run it locally in Jupyter (with the IRkernel) or open it in RStudio.

**Who it's for:** applied clinical and biomedical researchers and health data scientists. No heavy statistics background is needed, but some basic R helps.

## What's here

| Path | Contents |
|---|---|
| `hte_tutorial_notebook.ipynb` | The hands-on notebook (R), covering Segments 3–5 of the session |
| `slides/Brantner_DSHETutorial_HTE_10Sep2026.pptx` | Session slides |
| `data/simulated_mdd_trial.csv` | The simulated trial dataset the notebook reads (1,000 patients) |

### Notebook outline

- **Segment 3 — Data set-up and descriptives:** loading the data, the MADRS outcome, what "the treatment effect" means, a Table 1, and visual checks for effect moderators.
- **Segment 4 — Traditional approaches:** regression with a treatment × covariate interaction, and stratified (subgroup) analysis by age and baseline severity.
- **Segment 5 — Causal forests** with the [`grf`](https://grf-labs.github.io/grf/) package: patient-level CATE estimates, variable importance, an interpretation tree, and CATE plotted against covariates.
- **Stretch material:** testing for heterogeneity, best linear projection, uncertainty, and checking estimates against the simulated truth.

R packages used: `tidyverse`, `grf`, `rpart`, `rpart.plot`, `knitr`, `table1`, `gtsummary`.

## Data

The notebook reads a **simulated** trial dataset, [`data/simulated_mdd_trial.csv`](data/simulated_mdd_trial.csv), from this repository. It was created for the tutorial and first published at <https://github.com/v-rodriguez/Assessing-Heterogeneous-Treatment-Effects-Tutorial>. Because it is simulated, it includes each patient's true conditional average treatment effect (`true_cate`), so you can check the methods against the truth. The treatment arms carry real antidepressant names (vortioxetine vs duloxetine) only to make the example feel realistic. **The results are entirely made up and say nothing about the real-world effectiveness of either drug.**

## Part of the DSxHE tutorial series

- **Next in the series:** [Distributional cost-effectiveness analysis (DCEA)](https://github.com/Data-Science-for-Health-Equity/dcea-workshop)

## About the Data Diversity Theme

Health datasets often don't reflect the diversity of the populations they aim to serve, which can limit generalisability, reduce the effectiveness of new tools, and risk widening health inequalities. The [Data Diversity Theme](https://www.datascienceforhealthequity.com/themes/data-diversity), a partnership between Data Science for Health Equity and Cancer Research UK, brings together researchers, clinicians, funders and patient advocates to embed diversity across the research lifecycle. It is co-led by Dr Toral Gathani (University of Oxford) and Dr Brieuc Lehmann (UCL).

## Contact

Questions: [info@datascienceforhealthequity.com](mailto:info@datascienceforhealthequity.com)

## Licence

The materials in this repository are © 2026 Carly Brantner and released under the [Creative Commons Attribution 4.0 International licence (CC BY 4.0)](LICENSE). You may share and adapt them for any purpose, provided you give appropriate credit, for example:

> Brantner C (2026). *What Works for Whom: Assessing Heterogeneous Treatment Effects.* DSxHE Data Diversity × Statistical Methods Tutorial. https://github.com/Data-Science-for-Health-Equity/hte-tutorial
