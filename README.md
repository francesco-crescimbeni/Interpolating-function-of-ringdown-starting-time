# Description

Interpolating function of the ringdown starting time in the $(\eta,\chi_+,\chi_-)$ parameter for a given mismatch threshold, where $\eta=\frac{q}{(1+q^2)}$, $\chi_{+/-}=\frac{\chi_1\pm q\chi_2}{1+q}$, being $q$ the mass ratio and $(\chi_1,\chi_2)$ the spins of the binary progenitors.
Available ringdown models used for the interpolator:
- **London**, [arXiv:1810.03550](https://arxiv.org/abs/1810.03550);
- **Cheung**, [arXiv:2310.04489](https://arxiv.org/abs/2310.04489);
- **TEOBPM**, [arXiv:1406.0401](https://arxiv.org/abs/1406.0401).

The procedure to obtain the interpolant is the following.

1. For a given ringdown model, the mismatch between model and Numerical Relativity (NR) data is computed, for different harmonics and different starting times (see Eq. 17 of [https://arxiv.org/abs/2511.02915]). For the NR data, we use the SXS catalog (https://data.black-holes.org/simulations/index.html). The results are provided in this gitHub repository in avg_mismatches_all_times.npz and SXS_BBH_nonprec_nonecc_all.txt.

2. For a given model and $(\ell,|m|)$ harmonic, we choose a mismatch threshold, and we extrapolate its associated starting time.
  
4. We repeat this for all the SXS simulations.

5. Then, we obtain a scatter plot of $t_{\rm start}(\eta,\chi_+,\chi_-|\mathcal{M}_{\rm th})$ ([notebook 1](https://colab.research.google.com/github/francesco-crescimbeni/Interpolating-function-of-ringdown-starting-time/blob/main/t_start_eta_chip_chim_scatter.ipynb)).

6. Then, we perform an interpolation in the progenitor parameter space ([notebook 2](https://colab.research.google.com/github/francesco-crescimbeni/Interpolating-function-of-ringdown-starting-time/blob/main/t_start_eta_chip_chim_interpolant_frames.ipynb)).

The results of points 5. and 6. are already available in the 'plots' folder.

# Contact
For any questions or issues, please contact francesco.crescimbeni@uniroma1.it and gregorio.carullo@ligo.org.
