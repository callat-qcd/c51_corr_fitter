# c51_corr_analysis
The Collaboration 51 Correlation Function Analysis Suite.

This fitter is designed to analyze correlation functions generated from lattice QFT calculations.  This fitting package is currently undergoing rapid development, and there is no promise of backwards compatibility yet.  Version numbers will be used to support reproducibility.

- [Installation](#installation)
- [Example Usage](#example-usage)
- [Input File Description](#input-file-info)
- [Copyright Notice](#copyright-notice)

## Installation
This package requires the [lsqfit](https://github.com/gplepage/lsqfit) and [gvar](https://github.com/gplepage/gvar) libraries developed by Peter Lepage.

This package is now locally pip-installable in `editable` mode (which means, you can actively develop the code and re-install quickly).  Tested locally with a clean anaconda installation, the following works for installing on a mac OS at least.

```
[skip these steps unless you want to test a "clean" install]
conda create -n bare3.8 python=3.8
conda activate bare3.8

[rest of the install]
git clone https://github.com/callat-qcd/c51_corr_fitter
cd c51_corr_fitter
pip install -e .
```
This will result in an installation that claims there are pip install errors, but in practice, the installation works.  To test success, type
```
which fit_twopt
```
and if this returns a binary, the installation has worked.




## Example Usage

To build up a fit, one usually looks at effective mass plots etc., and starts to guess the input ground state energy and overlap factors.  With a working installation, you should be able (from the source directory) do
```
cd tests
fit_twopt input_file/callat_a12m220XL_test_params.py --eff --fit
```
which will generate effective mass plots and perform the fit of the states specified in the input file which is included in the `tests/data` directory.

## Input File Info


# Copyright Notice


Collaboration 51 Correlation Function Analysis Suite (c51_corr_analysis) 
Copyright (c) 2022, The Regents of the University of California, through 
Lawrence Berkeley National Laboratory (subject to receipt of any required 
approvals from the U.S. Dept. of Energy). All rights reserved.

If you have questions about your rights to use or distribute this software,
please contact Berkeley Lab's Intellectual Property Office at
IPO@lbl.gov.

NOTICE.  This Software was developed under funding from the U.S. Department
of Energy and the U.S. Government consequently retains certain rights.  As
such, the U.S. Government has been granted for itself and others acting on
its behalf a paid-up, nonexclusive, irrevocable, worldwide license in the
Software to reproduce, distribute copies to the public, prepare derivative 
works, and perform publicly and display publicly, and to permit others to do so.
