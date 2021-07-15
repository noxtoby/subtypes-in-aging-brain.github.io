# Event Based Model

<img src="../../_static/img/ebm.png" width="320px" alt="EBM from (Oxtoby et al., Brain 2021)">

## Background
The event-based model (EBM) of disease progression was invented in 2011 by Hubert Fonteijn and Danny Alexander. Hubert's [IPMI 2011 conference paper](https://doi.org/10.1007/978-3-642-22092-0_61) won the prestigious [Erbsmann Prize](https://en.wikipedia.org/wiki/Information_Processing_in_Medical_Imaging#Past_Francois_Erbsmann_Prize_Winners), and was published in full form in [this NeuroImage 2012 article](https://doi.org/10.1016/j.neuroimage.2012.01.062) using a small dataset from two rarer inherited neurodegenerative diseases: familial Alzheimer's disease and Huntington's disease.

The EBM methodology was generalised to sporadic disease by Alex Young and colleagues in her [2014 Brain paper](https://doi.org/10.1093/brain/awu176) and has since seen wide application (and methodological updates) across multiple neurodegenerative diseases including [familial Alzheimer's disease](https://doi.org/10.1093/brain/amy050), [Huntington's disease](https://doi.org/10.1002/acn3.558), [posterior cortical atrophy](https://doi.org/10.1093/brain/awz136) (also [here](https://doi.org/10.1002/alz.12083)), [Parkinson's disease](https://doi.org/10.1093/brain/awaa461), [Down sydrome](https://doi.org/10.1002/acn3.571), [amyotrophic lateral sclerosis](https://doi.org/10.1002/acn3.51035), and more.

The EBM is uniquely capable of estimating an ordered sequence of disease progression events, along with uncertainty in that ordering, using only cross-sectional data --- a single visit per patient. This is powerful for two reasons. First, disease progression can be estimated from smaller, and more widely-available cross-sectional datasets. Second, in real-world (future) clinical applications, new patients can be assessed on the spot at their first visit --- without the need for any patient history, nor the need to wait for a follow-up visit that might require them to wait in uncertainty for a year or more. Of course, the limitation of using only cross-sectional data is that _timescales_ of disease progression are much harder to estimate without further information.

You might ask "How is it possible to estimate a sequence of disease progression events from a single visit across multiple patients?"

The concept behind the EBM is quite simple and is based on one key assumption: disease progression is irreversible. This assumption is valid in chronic, progressive diseases if there is no disease-modifying intervention. To explain the concept, we borrow here from the analogy in [(Oxtoby, et al., Brain 2021)](https://doi.org/10.1093/brain/awaa461): imagine that the common cold was a chronic irreversible condition. If all patients who present with the common cold have a cough, but only some of these also have a sneeze, then we would infer with very high confidence that coughing comes before sneezing in the disease progression sequence. Any variability across individuals would decrease the certainty in this conclusion. The EBM uses this concept across multiple symptoms (more generally, biomarkers) to both estimate the disease progression seqeunce, and uncertainty in the sequence.

An important assumption made in EBM is that the ordering of events is common for all the subjects in a dataset. However, neurodegenerative diseases such as Alzheimer’s disease are notoriously heterogeneous; pathologically as well as in their clinical presentation in patients. There are differences between different patients in terms of the pathways of progression, and the effect the progression has on a patient's cognition. Discriminative EBM (DEBM) model, invented in 2017 by Vikram Venkatraghavan and colleagues [IPMI 2017 conference paper](https://arxiv.org/abs/1702.06408) and later published as a journal article in [NeuroImage](https://doi.org/10.1016/j.neuroimage.2018.11.024), estimates the orderings robustly in the presence of such heterogeneity. Apart from estimating the sequence of events, DEBM also estimates the relative temporal distance between the events, as illustrated below.

<div style="text-align:center"><img src="../../_static/img/debm.png" width="450px" alt="DEBM from (Venkatraghavan et al., NeuroImage 2021)" /></div>

These improvements helped a DEBM based method end up as one of the winning methods of the coveted [TADPOLE challenge](https://tadpole.grand-challenge.org/). The robustness of DEBM was further verified in multi-centre studies in [AD](https://doi.org/10.1016/j.nicl.2019.101954) and [genetic FTD](http://dx.doi.org/10.1136/jnnp-2020-323541).

## Getting started:

- To see what the model is capable of:
  - [ico**brain dm**](https://icometrix.com/services/icobrain-dm) from the [EuroPOND consortium](http://europond.eu).<br/>
  The EBM is embedded within the ico**brain dm** clinical tool as an experimental report.

- Take a look at the python code from the [UCL POND group](https://github.com/ucl-pond) on GitHub:
  - [normal EBM](https://github.com/ucl-pond/ebm) from ([Young et al., Brain 2014](https://doi.org/10.1093/brain/awu176))
  - [KDE EBM](https://github.com/noxtoby/kde_ebm_open) from ([Firth et al., Alzheimers Dement 2020](https://doi.org/10.1002/alz.12083)). This is a more flexible version capable of handling skewed biomarker data by using kernel density estimation (KDE) mixture modelling instead of Gaussian mixture modelling.

- An integrated python toolbox for DEBM and EBM  developed by Vikram Venkatraghavan can be accessed [here](https://github.com/88vikram/pyebm). This toolbox also capable of efficiently analyzing the effects of certain genetic factors on nerodegeneration as published recently in [Venkatraghavan et al., NeuroImage 2021](https://doi.org/10.1016/j.neuroimage.2020.117646)

- Some scientific papers about the EBM method:
  - [Fontiejn, et al., NeuroImage 2012](https://doi.org/10.1016/j.neuroimage.2012.01.062)
  - [Young, et al., Brain 2014](https://doi.org/10.1093/brain/awu176)
  - [Firth, et al., Alzheimer's & Dementia 2020](https://doi.org/10.1002/alz.12083)
