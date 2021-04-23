# Face Image Quality Assessment

NOTE: this IQM is now added to the ["full stack repository"](https://github.com/Kjetilgr/bachelor-full-stack)

This repository contains the [original repository](https://github.com/pterhoer/FaceImageQuality), ~~the repository [insightface](https://github.com/deepinsight/insightface/tree/60bb5829b1d76bfcec7930ce61c41dde26413279),~~ and the Face Recognition model [LResNet100E-IR,ArcFace@ms1m-refine-v2](https://github.com/deepinsight/insightface/wiki/Model-Zoo#31-lresnet100e-irarcfacems1m-refine-v2)

## Installation instructions

NOTE: The original code has only been tested and confirmed working on [windows](https://github.com/pterhoer/FaceImageQuality/issues/7)

First, clone this repository.

### Installing insightface

To make the code run, an [old version](https://github.com/deepinsight/insightface/tree/60bb5829b1d76bfcec7930ce61c41dde26413279) of the insightface repository is required. See why in [this issue](https://github.com/pterhoer/FaceImageQuality/issues/28)

Because of the file size, insightface needs to be downloaded separately.

Clone the [repository](https://github.com/deepinsight/insightface)

cd into the insigthface directory and reset the repository to the old commit mentioned above, using

```terminal
git reset --hard 60bb5829b1d76bfcec7930ce61c41dde26413279
```

Move the insightface directory into the FaceImageQuality directory: FaceImageQuality/insightface

### Installing the required packages

cd into the FaceImageQuality directory.

Use Anaconda to create a virtual environment and install the required packages

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

To show all conda environments (and confirm that the environment 'serfiq' exists)

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

Be aware that it may take a few minutes for the algorithm to finish the first time you run it.

## Known issues

### Geforce RTX 2080 issues

Using an RTX 2080 GPU may not work because of some package requirements.
