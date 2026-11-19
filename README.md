# Generative Image Synthesis — VAE & GAN Experiments

TensorFlow/Keras experiments covering grayscale signature synthesis with a variational autoencoder, dense GAN architectures, CIFAR-10 cat/dog image generation, and sketch/face translation scaffolding.

## Status

Academic prototype. Source reviewed; training and external services have not been rerun. No verified production deployment or benchmark is asserted.

## Contents

- `image_synthesis_experiments.ipynb`

## Setup

```sh
python -m venv .venv
# Activate your virtual environment
pip install -r requirements.txt
jupyter notebook
```

Dependencies reflect notebook imports and are not a tested version lock.

Provide authorized grayscale images at the configured data directory and paired sketch/face images for the later sections. CIFAR-10 is loaded through Keras. Update all placeholder and Colab paths before execution.

## Known limitations

The signature GAN and CIFAR-10 loops call discriminator training for the generator step; generator weights are not optimized there. The CIFAR-10 section references a discriminator before defining a compatible one. The sketch generator does not consume the input sketch. The CycleGAN section lacks cycle-consistency losses and gradient updates, and its generators output 64 channels rather than RGB. The Flask template is absent. This is an incomplete academic experiment, not a validated image translation service.

## Publication cleanup

Notebook outputs, execution counters, and incidental notebook metadata were removed. Assignment reports, datasets, archives, and nested assignment folder names are excluded. Original source files are preserved locally.
