# Face Image Quality Assessment

NOTE: see README-old.md for the original README

[This](https://github.com/deepinsight/insightface/tree/60bb5829b1d76bfcec7930ce61c41dde26413279) version of insightface is being used.

## Installation instructions

Clone the repository.

cd into the FaceImageQuality directory.

Please use Anaconda to install the required packages. This can be done by creating an virtual environment via

```terminal
conda env create -f environment.yml
```

To show all conda environments

```terminal
conda env list
```

Change conda environment

```terminal
conda activate serfiq
```

You should now be in the conda environment 'serfiq'. 

Test the IQM by running

```terminal
python serfiq_example.py
```