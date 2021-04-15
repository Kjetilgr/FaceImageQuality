# Face Image Quality Assessment

NOTE: see README-old.md for the original README

This repository contains the original repository, the repository [insightface](https://github.com/deepinsight/insightface/tree/60bb5829b1d76bfcec7930ce61c41dde26413279), and the Face Recognition model [LResNet100E-IR,ArcFace@ms1m-refine-v2](https://github.com/deepinsight/insightface/wiki/Model-Zoo#31-lresnet100e-irarcfacems1m-refine-v2)

Because of [this issue](https://github.com/pterhoer/FaceImageQuality/issues/28) an [older version](https://github.com/deepinsight/insightface/tree/60bb5829b1d76bfcec7930ce61c41dde26413279) of insightface is being used.

## Installation instructions

Clone the repository.

cd into the FaceImageQuality directory.

Use Anaconda to install the required packages. This can be done by creating an virtual environment via

```terminal
conda env create -f environment.yml
```

Or manually install the packages

```terminal
conda create -n serfiq python=3.6.9
conda install cudatoolkit
conda install cudnn
conda install tensorflow=1.14.0
conda install mxnet
conda install mxnet-gpu
conda install tqdm
conda install -c conda-forge opencv
conda install -c anaconda scikit-learn
conda install -c conda-forge scikit-image
conda install keras=2.2.4
```

To show all conda environments (and to check that the environment 'serfiq' exists)

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

## Known issues

### Conda virtual environment issues

Running the command

```terminal
conda env create -f environment.yml
```

Doesn't work on Mac or Linux

### Geforce RTX 2080 issues

Using an RTX 2080 GPU can cause errors
