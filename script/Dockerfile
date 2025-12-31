# Use Ubuntu 20.04 as the base (it supports Python 3.8 natively)
# Use a base that includes CUDA 11.2 and cuDNN 8 (standard for TF 2.5-2.10)
FROM nvidia/cuda:11.2.2-cudnn8-devel-ubuntu20.04

# Avoid prompts during installation
ENV DEBIAN_FRONTEND=noninteractive

# Install Python 3.8 and system dependencies
RUN apt-get update && apt-get install -y \
    python3.8 \
    python3.8-dev \
    python3.8-venv \
    python3-pip \
    wget \
    git \
    && rm -rf /var/lib/apt/lists/*

# Set Python 3.8 as the default python
RUN update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 1

WORKDIR /app

CMD ["python3"]