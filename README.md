# Optimal Control of Grid-Interfacing Inverters With Current Magnitude Limits
This repository contains source code necessary to reproduce the results presented in the following paper:
[Optimal Control of Grid-Interfacing Inverters With Current Magnitude Limits](https://arxiv.org/abs/2310.00473)  

Authors: Trager Joswig-Jones and Baosen Zhang  

University of Washington 


# Motivation
Grid-interfacing inverters act as the interface between renewable resources and the electric grid, and have the potential to offer fast and programmable controls compared to synchronous generators. With this flexibility there has been significant research efforts into determining the best way to control these inverters. Inverters are limited in their maximum current output in order to protect  semiconductor devices, presenting a nonlinear constraint that needs to be accounted for in their control algorithms. Existing approaches either simply saturate a controller that is designed for unconstrained systems, or assume small perturbations and linearize a saturated system. These approaches can lead to stability issues or limiting the control actions to be too conservative.

In this paper, we directly focus on a nonlinear system that explicitly accounts for the saturation of the current magnitude. We use a Lyapunov stability approach to determine a stability condition for the system, guaranteeing that a class of controllers would be stabilizing if they satisfy a simple SDP condition. With this condition we fit a linear-feedback controller by sampling the output (offline) model predictive control problems. This learned controller has improved performances with existing designs.

# Language and Dependencies
This respository contrains code implemented in Python and can be run using Jupyter notebook or Google Colab. The code is also available on Google Drive at [https://drive.google.com/file/d/1LneERLmkHdRN5rU45h1dr_hdlvp6qKTx/view?usp=sharing](https://drive.google.com/file/d/1LneERLmkHdRN5rU45h1dr_hdlvp6qKTx/view?usp=sharing), which can be easily opened in Google Colab for execution.


## Acknowledgments

The development of this code was supported in part by NSF grant ECCS-2153937.

The primary developer is Trager Joswig-Jones (@TragerJoswig-Jones).

This source code is available in the hope that it will be useful, but without any warranty and in no event shall the authors or copyright holders be liable for any claim, damages or other liability.

## Notes

The captions of Fig. 3 and Fig. 4 have errors in the $x_0$ and $x^{\*}$ values. The correct values are $x_0 =$ ($0$ A, $0$ A), $x^{\*}$ = ($2.95$ A, $2.95$ A).

# Citing

If you find this repository useful in your work, we kindly request that you cite the following [publication](https://arxiv.org/abs/2310.00473):
```
@misc{joswigjones2023optimal,
      title={Optimal Control of Grid-Interfacing Inverters With Current Magnitude Limits}, 
      author={Trager Joswig-Jones and Baosen Zhang},
      year={2023},
      eprint={2310.00473},
      archivePrefix={arXiv},
      primaryClass={eess.SY}
}
```
