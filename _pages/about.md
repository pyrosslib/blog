---
layout: page
title: About
permalink: /about/
---

[PyRoss](https://github.com/rajeshrinet/pyross) is a numerical library that offers an integrated platform for **inference**, **forecasts** and **non-pharmaceutical interventions** in structured epidemiological compartment models.

**Compartment models** of arbitrary complexity can be  **user-defined** through Python dictionaries. The most common epidemiological models, and several less common ones, come pre-defined with the library. Models can include **stages** to allow for non-exponentially distributed compartmental residence times. Currently,  [pre-defined models](https://github.com/rajeshrinet/pyross/blob/master/docs/models.pdf) include ones with multiple disease states (exposed, asymptomatic, symptomatic, etc) and may be further divided by age, and by objective medical states (hospitalized, in ICU, etc). The compartment framework supports models for **disease surveillance** and **quarantine** and a variety of other processes of epidemiological relevance. 

**Generative processes** can be formulated **stochastically** (as Markov population processes) or **deterministically** (as systems of differential equations). Population processes are sampled exactly by the Doob-Gillespie algorithm or approximately by the tau-leaping algorithm while differential equations are integrated by both fixed and adaptive time-stepping. A **hybrid algorithm** transits dynamically between these  depending on the magnitude of the compartmental fluctuations. 

**Bayesian inference** on pre-defined or user-defined models is performed using model-adapted **Gaussian processes**  derived from **functional limit theorems** for Markov  population process. Generative models are fitted to data through the surveillance model allowing for possibily **unobserved** compartments. The **MAP** estimates of parameters and their standard errors can be obtained rapidly by optimising, obviating the need for expensive Markov chain Monte Carlo. This enables the fast evaluation of the **model evidence**, through which competing models may be **objectively compared** and their forecasts combined by **Bayesian model averaging**. Forecasts of disease progression, then, can be **fully Bayesian**, convolving uncertainties in data, parameters and models. The sensitivity of these forecasts is estimated through the **Fisher information matrix**. 

**Non-pharmaceutical interventions** are implemented as modifications of the **contact structures** of the model. **Optimised control** of these structures, given **cost functions**, is possible. This feature is being actively developed to be better integrated with the library.

[PyRossGeo](https://github.com/lukastk/PyRossGeo) is a companion library that supports **spatially resolved compartment models** with explicit **commuting networks**. [PyRossTSI](https://github.com/rajeshrinet/pyrossTSI) is another companion library for **time since infection models**. 

The libraries are named after [Sir Ronald Ross](https://en.wikipedia.org/wiki/Ronald_Ross), doctor, mathematician and poet. In 1898 he made "the great discovery" in his laboratory in Calcutta "that malaria is conveyed by the bite of a mosquito".  He won the Nobel Prize in 1902 and laid the foundations of the mathematical modelling of infectious diseases.


The authors are part of [The Rapid Assistance in Modelling the Pandemic (RAMP)](https://royalsociety.org/news/2020/03/urgent-call-epidemic-modelling/) taskforce at the **University of Cambridge**. In alphabetical order, we are:
[Ronojoy Adhikari](https://github.com/ronojoy),
[Austen Bolitho](https://github.com/TakodaS),
Fernando Caballero, Michael Cates,
[Jakub Dolezal](https://github.com/JakubJDolezal),
[Tim Ekeh](https://github.com/tekeh),
Jules Guioth, Robert Jack,
[Julian Kappler](https://github.com/juliankappler),
[Lukas Kikuchi](https://github.com/lukastk),
[Irene Li](https://github.com/Irene-Li),
Joseph Peterson,
[Patrick Pietzonka](https://github.com/ppietzonka),
[Benjamin Remez](https://github.com/BenjaminRemez),
[Paul Rohrbach](https://github.com/prohrbach),
[Rajesh Singh](https://github.com/rajeshrinet), 
and [Günther Turk](https://github.com/phi6GTurk).

Please read the  [PyRoss paper](https://arxiv.org/abs/2005.09625) and [PyRoss Wiki](https://github.com/rajeshrinet/pyross/wiki/) before you use PyRoss for your research. [Open an issue](https://github.com/rajeshrinet/pyross/issues), in preference to emailing us with queries. Join our [Slack channel](https://join.slack.com/t/pyross/shared_invite/zt-e8th6kcz-S4b_oJIZWPsGLruSPl3Zuw)  for discussion. Please follow the [Contributor Covenant](https://www.contributor-covenant.org/version/2/0/code_of_conduct/) in all PyRoss fora. Thank you!