# climpred CESM1 S2S Analysis

This repository holds a few notebooks to demonstrate how to generate anomalies from the raw CESM1-SubX S2S output and then use `climpred` to verify them against ERA5 data. 

Note that this showcases the procedure on Cheyenne/Casper, where `dask` workers were optimized for that infrastructure and I point to files on our storage system.

## Steps

If you don't have miniconda or anaconda installed in your home environment, you should do so.

1. Download the latest `miniconda` for Linux 64-bit: https://docs.conda.io/en/latest/miniconda.html.
2. `scp` the bash installed to your work or home directory on Cheyenne.
3. Run `bash Miniconda3-latest-Linux-x86_64.sh` to install miniconda to your command line.
4. During installation, allow it to edit your path in `~/.bashrc`. Restart your instance or do `source ~/.bashrc` and make sure that `conda --help` runs. If it doesn't, add `conda` to your path. (E.g., https://askubuntu.com/questions/849470/how-do-i-activate-a-conda-environment-in-my-bashrc)

Now that you have conda installed on your command line, clone this repository to your work directory and navigate there. Run `conda env update -f environment.yml` and it will install all the required packages under an environment called "S2S". When you open https://jupyterhub.ucar.edu/ and create a new notebook, you should see a grid tile for the S2S environment.

**When running all of these notebooks, click the drop-down menu in the top right and change the environment to the S2S environment**

Comments Judith: 
0.0_launch_cluster.ipynb is the launch script
0.01-0.04 are "pre-processing scripts and need to be run for most applications
0.05 is the script for the actual verification. It contains the steps necessary for 
dealing with Feb 29. 
For new scripts, I suggest copying 0.05 and start to replace under title 'Verification'.

## Figures

Here are a few figures that come out of this quick analysis.

### Anomaly Correlation Coefficient for lead days 0-9

![](https://i.imgur.com/ObiLmKg.png)

### Anomaly Correlation Coefficient for lead days 30-39

![](https://i.imgur.com/LGrGfZj.png)

### RMSE for lead days 10-19

![](https://i.imgur.com/ymE53yp.png)

### Globally averaged TAS anomaly correlation coefficients by initialization month

![](https://i.imgur.com/ZcAF5X3.png)



