# MICCAI 2021



```{figure} ../../_static/img/conferences/MICCAI_2021.png
---
name: MICCAI
align: center
width: 70%
---
**MICCAI 20201**.
```

````{panels}
:column: col-12
:card: border-2 shadow
:header: bg-warning
**Workshop abstract**
^^^
The proposed tutorial is intended to present the most advanced and mature data-driven models for the modelling of neurological disease progression within a day-long session. The main objective is to illustrate the major challenges of modelling neurodegenerative disorders, especially the unknown (and heterogeneous) disease time axis, and, the reconstruction of long-term disease history from short-term individual observations - challenges existing beyond neurological applications. To that end, the tutorial will dive into state-of-the-art models that allows to take the best out of cross-sectional and longitudinal data. Short lectures introducing the intention of each DPM model will be followed by hands-on session based on Python notebooks that illustrate the different concepts in the context of Alzheimer's disease progression. At the end, the participants will be able to select a DPM model suitable to their own dataset and implement it thanks to the software presented.

{badge}`Conference workshop,badge-primary`
{badge}`Hands-on session,badge-primary`
{badge}`Full day,badge-primary`
````

[Link to the conference](https://www.miccai2021.org/en)

## Learning objectives of the tutorial

1. Discover the main challenges of DPM thanks to the estimation of Alzheimer’s disease progression  at group and individual levels,
2. Understand the rationale behind different state-of-the-art DPM methods and their limitations,
3. Acquire operational knowledge for selecting a DPM suitable to any given dataset, and be able to implement it with the right software,
4. Get an in-depth overview of the operational challenges of longitudinal data, along with the ‘know-hows’ to overcome them

## Schedule

`Introduction to Disease Progression Modelling /`

`Part 1: Discrete DPM / ` by _Neil Oxtoby & Vikram Venkatraghavan_ • 1h30

: Discrete models are capable of inferring a longitudinal picture of disease progression using only cross-sectional data. [Europond : github link](https://github.com/EuroPOND/europond-software).

`Part 2: Linear Mixed-effects models / ` 1h30

: The workhorse of statistical analysis for longitudinal data. Important to understand their capabilities and limitations for analysing neurological disease progression.

`Part 3: Parametric continuous DPM / ` by _Igor Koval & Stanley Durrleman_ • 1h30

: Recent developments that address some limitations of Linear Mixed-effects methods account for the non-linear dynamics of progression. They are able to estimate a long-term history of changes based on longitudinal observations, referred to as a disease course mapping.  [Leaspy repository](https://gitlab.com/icm-institute/aramislab/leaspy)

`Part 4: Non-parametric continuous DPM / ` by _Sara Garbarino, Clément Abi Nader, Marco Lorenzi_ • 1h30

: DPM based on dynamical system modelling allow estimating the dynamics of biomarkers’ interactions characterizing the long-term disease history.  Building upon probabilistic DPM (Lorenzi-NeuroImage-2017),  these methods have been applied to the modelling of pathological protein propagation across brain networks in Alzheimer’s (Garbarino-IPMI-2019), and to simulate the effect of amyloid intervention on long term clinical and imaging outcomes (Abi Nader -preprint- 2020). [GP progression repository](https://gitlab.inria.fr/epione/GP_progression_model_V2).

`Wrap-up & Conclusion`
