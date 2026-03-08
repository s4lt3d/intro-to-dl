# Introduction to Deep Learning

> Course materials and Jupyter notebooks for the Coursera Introduction to Deep Learning course, with setup instructions for Google Colab, Docker, and Anaconda.

---

## Overview

This repository contains complete course materials for [Coursera's Introduction to Deep Learning](https://www.coursera.org/learn/intro-to-deep-learning), including Jupyter notebooks covering neural networks, convolutional networks, recurrent networks, and practical deep learning applications.

---

## Quick Start

**Recommended:** Use [Google Colab](https://colab.research.google.com) with free GPU access:

1. Go to https://colab.research.google.com and sign in
2. Click **GITHUB** tab, paste `https://github.com/hse-aml/intro-to-dl` and press Enter
3. Choose a notebook (e.g., `week2/v2/mnist_with_keras.ipynb`)
4. Click **File → Save a copy in Drive...** to save progress
5. Click **Runtime → Change runtime type** and select **GPU**
6. In the first cell, run:
```python
! shred -u setup_google_colab.py
! wget https://raw.githubusercontent.com/hse-aml/intro-to-dl/master/setup_google_colab.py -O setup_google_colab.py
import setup_google_colab
# Uncomment the week you're working on:
# setup_google_colab.setup_week1()
# setup_google_colab.setup_week2()
# etc.
```

**Colab Known Issues:**
- No `ipywidgets` support (simplified progress bars used instead)
- Some animation flicker with `IPython.display.clear_output()`

---

## Local Setup

Coursera Jupyter can be slow. For better performance, run locally with Docker or Anaconda (requires 4GB+ RAM).

### Docker (Mac/Linux) - Recommended

Follow instructions at: https://hub.docker.com/r/zimovnov/coursera-aml-docker/

GPU support (Linux only): https://github.com/ZEMUSHKA/coursera-aml-docker#using-gpu-in-your-container-linux-hosts-only

### Anaconda (Windows/Mac/Linux)

1. Install [Anaconda with Python 3.5+](https://www.anaconda.com/download)
2. Download [`conda_requirements.txt`](https://github.com/ZEMUSHKA/coursera-aml-docker/blob/master/conda_requirements.txt)
3. Run in terminal:
```bash
conda config --append channels conda-forge
conda config --append channels menpo
conda install --yes --file conda_requirements.txt
jupyter notebook
```

### Download Course Materials

In Jupyter, click **New → Terminal** and run:
```bash
git clone https://github.com/hse-aml/intro-to-dl.git
```

Then open `intro-to-dl` folder, run `download_resources.ipynb` for your week, and start coding.

### GPU Support (Advanced - Anaconda)

Requires NVIDIA driver, CUDA toolkit, and cuDNN. See [TensorFlow GPU setup](https://www.tensorflow.org/versions/r1.2/install/install_linux#nvidia_requirements_to_run_tensorflow_with_gpu_support).

---

## Course Structure

The course is organized by weeks, each with lectures, assignments, and practice notebooks:

- **Week 1** — Intro to deep learning, TensorFlow basics, neural network fundamentals
- **Week 2** — Convolutional neural networks (CNNs), image classification with MNIST/CIFAR
- **Week 3** — Recurrent neural networks (RNNs), sequence modeling, text generation
- **Week 4** — Advanced topics, optimization, regularization, practical techniques
- **Weeks 5+** — Specialized topics, applications, and final projects

---

## Key Topics Covered

- Neural network architecture and training
- Backpropagation and optimization algorithms
- Convolutional networks for computer vision
- Recurrent networks for sequences
- Transfer learning and fine-tuning
- Practical deep learning techniques

---

## Requirements

- Python 3.5+ (3.7+ recommended)
- Jupyter Notebook or Google Colab
- TensorFlow 2.0+
- NumPy, Matplotlib, and other common ML libraries

---

## Course

[Coursera - Introduction to Deep Learning](https://www.coursera.org/learn/intro-to-deep-learning)
