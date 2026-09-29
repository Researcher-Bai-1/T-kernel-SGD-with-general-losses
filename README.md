# T-kernel SGD with General Losses

This repository contains the experimental code for:

**Jinhui Bai, Andreas Christmann, and Lei Shi.**  
*Truncated Kernel Stochastic Gradient Descent with General Losses and Spherical Radial Basis Functions.*

**Paper:** [arXiv:2510.04237](https://arxiv.org/abs/2510.04237)

## Code and paper correspondence

The section and figure numbers below follow [arXiv v7](https://arxiv.org/abs/2510.04237v7). The notebooks compute the numerical results for the corresponding experiments.

| Paper location | Experiment / method | Notebook |
| --- | --- | --- |
| Section 4.1, Example 1; Figure 1 | Circle regression: T-kernel SGD | [general_loss_subsection4.1_example1.ipynb](general_loss_subsection4.1_example1.ipynb) |
| Section 4.1, Example 1; Figure 1 | Circle regression: kernel SGD | [general_loss_subsection4.1_example1_kernel_sdg.ipynb](general_loss_subsection4.1_example1_kernel_sdg.ipynb) |
| Section 4.1, Example 1; Figure 1 | Circle regression: Nyström | [general_loss_subsection4.1_example1_Nystrom.ipynb.ipynb](general_loss_subsection4.1_example1_Nystrom.ipynb.ipynb) |
| Section 4.1, Example 2; Figure 2 | Circle regression: T-kernel SGD | [general_loss_subsection4.1_example2.ipynb](general_loss_subsection4.1_example2.ipynb) |
| Section 4.1, Example 2; Figure 2 | Circle regression: kernel SGD | [general_loss_subsection4.1_example2_kernel_sdg.ipynb.ipynb](general_loss_subsection4.1_example2_kernel_sdg.ipynb.ipynb) |
| Section 4.1, Example 2; Figure 2 | Circle regression: Nyström | [general_loss_subsection4.1_example2_Nystrom.ipynb.ipynb](general_loss_subsection4.1_example2_Nystrom.ipynb.ipynb) |
| Section 4.1.1; Figure 3 | Sensitivity to regularity, capacity, truncation, and projection radius | [sensitivity_analysis.ipynb](sensitivity_analysis.ipynb) |
| Section 4.2; Figure 4 | Regression on the sphere: T-kernel SGD | [general_loss_subsection4.2.ipynb](general_loss_subsection4.2.ipynb) |
| Section 4.2; Figure 4 | Regression on the sphere: kernel SGD | [general_loss_subsection4.2_kernel_sgd.ipynb](general_loss_subsection4.2_kernel_sgd.ipynb) |
| Section 4.3; Figure 5 | MNIST odd/even classification: T-kernel SGD | [general_loss_subsection4.3.ipynb](general_loss_subsection4.3.ipynb) |
| Section 4.3; Figure 5 | MNIST odd/even classification: kernel SGD | [MNIST_kernel_SGD.ipynb](MNIST_kernel_SGD.ipynb) |
| Section 4.4; Figure 6 | GRACE satellite data | [general_loss_subsection4.4addition.ipynb](general_loss_subsection4.4addition.ipynb) |
| Section 4.5; Figure 7 | Regression with spherical diffusion balance | [general_loss_subsection4.5addition.ipynb](general_loss_subsection4.5addition.ipynb) |

## Data files

The following GRACE data files are used in Section 4.4 (Figure 6).

| File | Month |
| --- | --- |
| `GSM-2_2003001-2003031_GRAC_UTCSR_BA01_0600` | January 2003 |
| `GSM-2_2003091-2003120_GRAC_UTCSR_BA01_0600` | April 2003 |
| `GSM-2_2003182-2003212_GRAC_UTCSR_BA01_0600` | July 2003 |
| `GSM-2_2003274-2003304_GRAC_UTCSR_BA01_0600` | October 2003 |

[Data dictionary](Data%20dictionary) describes the MNIST and GRACE datasets. MNIST is downloaded automatically through torchvision; synthetic data are generated within the corresponding notebooks.

## Running the experiments

Install the required Python packages:

```bash
python -m pip install numpy scipy matplotlib torch torchvision jupyterlab
```

Download or clone this repository, start JupyterLab from the repository root, and open the notebook for the desired experiment:

```bash
python -m jupyterlab
```

Run each notebook in a separate kernel and execute its cells in order. Keep the four GRACE files in the same directory as the GRACE notebook. Experiment parameters are specified in the notebooks; the resulting errors, accuracies, and runtimes are printed or stored in notebook variables.
