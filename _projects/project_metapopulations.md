---
layout: page
title: metapopulations
description: dynamics of metapopulation disease models
img: assets/img/figure_variant_importation_base_model_with_stimulations.png
importance: 1
category: current
---

Most of my work in the area of the spatio-temporal spread of diseases uses metapopulations. In a metapopulation framework, space is divided into geographical units called patches. Suppose we use $n$ such units. Each unit has a certain number of susceptible and infectious individuals, which we denote $S_p(t)$ and $I_p(t)$ in patch $p=1,\ldots,n$. Further, parameters can vary from patch to patch. For example, a patch which is in a richer region might have a better health care system, leading to less time spent as infectious before recovering. A metapopulation model "equivalent" to the PDE above would then take the following form: 
\begin{align*} 
\frac{d}{dt}S_p &= -\beta_p S_pI_p +\sum_{q=1}^n m_{pq}^SS_q\\ 
\frac{d}{dt}I_p &= \beta_p S_pI_p-\mu_p I_p+\sum_{q=1}^n m_{pq}^II_q. 
\end{align*} 
Here, parameters play the same role as those used in the PDE, except that we replace the rates of diffusion $D_S$ and $D_I$ by rates of movement $m_{pq}^S$ and $m_{pq}^I$; $m_{pq}^S$, for example, is the rate of movement of individuals from patch $q$ to patch $p$. Concerning $m_{pp}$, we assume that 
\[ 
m_{pp}=-\sum_{q=1}^n m_{qp},
\] 
which allows us to formulate the model in this simple way.

Most of the models I have considered in this context are not of Kermack-McKendrick type: they include demography (birth and death). Also, they often include a more detailed description of disease processes, by considering an SLIRS structure, i.e., one where individuals are susceptible, latently infected (infected but not yet infectious), infectious or recovered (temporarily immune). A model in that context takes the following form: 
\begin{align*} 
\frac{d}{dt}S_{sp} &= \mathcal{B}_{sp}-d_{sp}S_{sp}-f_{sp}(S_{sp},I_{sp},N_{sp}) +\sum_{q=1}^n m_{pq}^SS_q\\ 
\frac{d}{dt}I_{sp} &= f_{sp}(S_{sp},I_{sp},N_{sp})-(d_{sp}+\delta_{sp})I_{sp}+\sum_{q=1}^n m_{pq}^II_q. 
\end{align*}