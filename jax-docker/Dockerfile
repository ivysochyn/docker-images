# syntax=docker/dockerfile:1
FROM nvidia/cuda:11.8.0-cudnn8-devel-ubuntu20.04

ENV PIPINST 'python3 -m pip install --no-cache-dir --upgrade'
ENV INST 'env DEBIAN_FRONTEND=noninteractive apt-get install -y'

RUN apt-get update && apt-get upgrade -y && \
    $INST \
    git \
    jupyter-notebook \
    python3-dev \
    python3-flake8 \
    python3-pip \
    vim \
    xterm \
    && rm -rf /var/lib/apt/lists/*

RUN $PIPINST "jax[cuda11_pip]" -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html
