# A Multi-pass Land Data Assimilation Scheme (MLDAS) based on Noah-MP-Crop model
[![DOI](https://img.shields.io/badge/DOI-10.5281/zenodo.3856486-blue.svg)](https://doi.org/10.5281/zenodo.3856486)

The leaf area index (LAI), soil moisture, and solar-induced chlorophyll fluorescence (SIF) observations are simultaneously assimilated into the Noah-MP-Crop model based on the MLDAS to predict sensible (H) and latent (LE) heat fluxes as well as gross primary productivity (GPP).
The code demonstrates the Keras implementation of the MLDAS as proposed in paper "MLDAS: A Multi-pass Land Data Assimilation Scheme for Improving Performances of Noah-MP-Crop Model through Jointly Assimilation of Leaf Area Index, Soil Moisture, and Solar‐Induced Chlorophyll Fluorescence Observations"  published in *JGR*. [[link to the paper]](https://)

Please refer to the file `License.txt` for the license governing this code.

If you use this repository in your work, please cite:

> Xu, T.R., He, X.L., Chen, F., et al. (2020) MLDAS: A Multi-pass Land Data Assimilation Scheme for Improving Performances of Noah-MP-Crop Model through Jointly Assimilation of Leaf Area Index, Soil Moisture, and Solar‐Induced Chlorophyll Fluorescence Observations


If you have any questions or suggestions with the code, please let us know. Contact Tongren Xu at *xutr@bnu.edu.cn* and Xinlei He at *hxlbsd@mail.bnu.edu.cn*

------

## Quick Start

The code was tested with Python 3.7. To use this code, please do:

1. Clone the repo:

   ```shell
   git clone https://github.com/oreopie/physics-aware-dl.git
   cd physics-aware-dl
   ```

2. Install dependencies:

   ```shell
   module load python/3.7.5
   pip install --user numpy
   pip install --user pandas
   pip install --user netCDF4
   ```

3. Download CAMELS (Catchment Attributes and Meteorology for Large-sample Studies) data set  `CAMELS time series meteorology, observed flow, meta data (.zip) `  from [https://ral.ucar.edu/solutions/products/camels](https://ral.ucar.edu/solutions/products/camels). Unzip `basin_timeseries_v1p2_metForcing_obsFlow.zip` and reorganize the directory as follows,

   ```
   camels\
   |---basin_mean_forcing\
   |   |---daymet\
   |       |---01\
   |       |---...	
   |       |---18	\
   |---usgs_streamflow\
       |---01\
       |---...	
       |---18\
   ```

4. Start `Jupyter Notebook` and run the `demo_single.ipynb` locally.
