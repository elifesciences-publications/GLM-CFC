# GLM-CFC
A GLM based approach to assess CFC.

Code to measure cross-frequency coupling between two signals as described in this manuscript: 

J. Nadalin, L-E Martinet, et al., 2019. A statistical framework to assess cross-frequency coupling while accounting for confounding analysis effects, eLife, https://doi.org/10.7554/eLife.44287

See also the [preprint](https://www.biorxiv.org/content/10.1101/519470v2).


`ExampleCode.m`: Run the cells in this file to produce example voltage traces and surfaces in (Phi_low, A_low, A_high)-space (as in Figure 4 of the manuscript). Four simulations are present: (i) no CFC, (ii) PAC only, (iii) AAC only, and (iv) both PAC and AAC.

`simfun.m`: Code to simulate signals V_low, V_high, with induced cross-frequency coupling and measure output statistics R_PAC and R_AAC along with confidence intervals and p-values.

`glmfun.m`: Code to evaluate the coupling statistics R_PAC and R_AAC, along with confidence intervals and p-values, between two signals.

`glmfun_with_indicator.m`: Cn example of how to update glmfun to test for effect of condition (e.g. pre and post stimuli) on coupling

The voltage traces for the human data can be found in `Patient_Data.mat`, and the rodent data can be found at https://github.com/tne-lab/cl-example-data

The [Chaotic System Toolbox](https://www.mathworks.com/matlabcentral/fileexchange/1597-chaotic-systems-toolbox) is required to generate surrogate data.

Any questions/comments please direct to Jessica Nadalin (jnadalin@bu.edu) or Mark Kramer (mak@bu.edu)
