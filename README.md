# The authors' official PyTorch SigCGAN implementation.

This repository is the official implementation of [Conditional Sig-Wasserstein GANs for Time Series Generation]

Authors:

Paper Link:

## Requirements

To setup the conda enviroment:

```setup
conda env create -f requirements.yml
```

## Dataset

This repository contains implementations of synthetic dataset generated by VAR model and one emperical dataset. Data generation functions are in sig_lib/data.py

-    VAR data: Synthetic data
-    Stock data: https://realized.oxford-man.ox.ac.uk/data

## Baselines

We compare our SigCGAN with several baselines including: TimeGAN, RCGAN, GMMN(GAN with MMD). The baselines functions are in sig_lib/baselines.py


## Training

To train the model(s), save weights and produce a training summaries, run this command for GPU training:

```train
python train.py -use_cuda
```
Optionally drop the flag ```-use_cuda``` to run the experiments on CPU.


## Evaluation

To evaluate models on different metrics and GPU, run:

```eval
python evaluation.py -use_cuda
```
As above, optionally drop the flag ```-use_cuda``` to run the evaluation on CPU.

## Numerical Results

The numerical results will be saved in the 'numerical_results' folder during training process. Running evaluation.py will produces the 'summary.csv' files.
