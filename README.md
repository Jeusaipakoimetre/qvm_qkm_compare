# QVM/QKM comparison

## Introduction

This project is based on the work of *José Miguel Monzón-Verona*, *Santiago García-Alonso* and *Francisco Jorge Santana-Martín* titled "**Quantum Variational vs. Quantum Kernel Machine Learning Models for Partial Discharge Classification in Dielectric Oils**", and can be found here: https://doi.org/10.3390/s25041277

The attempt is to extend the part of the conclusion where they highlight the fact that the QKM hybrid method appeared to work slightly better on their particular case than the QVM one. Indeed, this notebook aim to create an easy tool to compare both methods without having to modify the entire code on each test.

## Run

It is recommanded to create a python virtual environment (https://docs.python.org/3/library/venv.html) so that you can cleanly install the requirements in `requirements.txt`.

Next, you can open the notebook (`code/qvm_qkm_compare.ipynb`), and run it in its entirety. It should execute everything without showing any errors, so if at this point there's something wrong it's not intended.

The notebook shouldn't take long to run entirely because, by default, all "expensive" operations are disabled. Indeed, the result of these operations is already saved in different files in the `code` directory.

If you want to compute new results with a new dataset/parameters, you should first change the options in the three "**Parameters**" sub-sections (one global, and two for respectively QVM and QKM). The code will automatically detect if this configurations has already been calculated, if so the corresponding file will be loaded instead of recalculating everything. You can always force an overwrite of this behavior by making the corresponding boolean equal to True in the "**Re-run**" section.

Any new implementation (new dataset, new parameter change in the training) should use this parameter system so that the notebook keeps its ease of use and of modifications
