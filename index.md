---
layout: home
search_exclude: true
---

![Imagel](https://raw.githubusercontent.com/rajeshrinet/pyross/master/examples/banner.jpg)

[PyRoss](https://github.com/rajeshrinet/pyross) is a numerical library that offers an integrated platform for **inference**, **forecasts** and **non-pharmaceutical interventions** in structured epidemiological compartment models.

**Compartment models** of arbitrary complexity can be  **user-defined** through Python dictionaries. The most common epidemiological models, and several less common ones, come pre-defined with the library. Models can include **stages** to allow for non-exponentially distributed compartmental residence times. Currently,  [pre-defined models](https://github.com/rajeshrinet/pyross/blob/master/docs/models.pdf) include ones with multiple disease states (exposed, asymptomatic, symptomatic, etc) and may be further divided by age, and by objective medical states (hospitalized, in ICU, etc). The compartment framework supports models for **disease surveillance** and **quarantine** and a variety of other processes of epidemiological relevance. 

**Generative processes** can be formulated **stochastically** (as Markov population processes) or **deterministically** (as systems of differential equations). Population processes are sampled exactly by the Doob-Gillespie algorithm or approximately by the tau-leaping algorithm while differential equations are integrated by both fixed and adaptive time-stepping. A **hybrid algorithm** transits dynamically between these  depending on the magnitude of the compartmental fluctuations. 

**Bayesian inference** on pre-defined or user-defined models is performed using model-adapted **Gaussian processes**  derived from **functional limit theorems** for Markov  population process. Generative models are fitted to data through the surveillance model allowing for possibily **unobserved** compartments. The **MAP** estimates of parameters and their standard errors can be obtained rapidly by optimising, obviating the need for expensive Markov chain Monte Carlo. This enables the fast evaluation of the **model evidence**, through which competing models may be **objectively compared** and their forecasts combined by **Bayesian model averaging**. Forecasts of disease progression, then, can be **fully Bayesian**, convolving uncertainties in data, parameters and models. The sensitivity of these forecasts is estimated through the **Fisher information matrix**. 

**Non-pharmaceutical interventions** are implemented as modifications of the **contact structures** of the model. **Optimised control** of these structures, given **cost functions**, is possible. This feature is being actively developed to be better integrated with the library.