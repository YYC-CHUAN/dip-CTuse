**Warning!** The optimization may not converge on some GPUs. We've personally experienced issues on Tesla V100 and P40 GPUs. When running the code, make sure you get similar results to the paper first. Easiest to check using text inpainting notebook.  Try to set double precision mode or turn off cudnn. 

# CT Image Reconstruction and Optimization with Unsupervised Deep Learning

In this repository we provide *Jupyter Notebooks* to reproduce each figure from the paper:

> **CT Image Reconstruction and Optimization with Unsupervised Deep Learning**

> Yanchuan Yin

# Install

Here is the list of libraries you need to install to execute the code:
- python = 3.6
- [pytorch](http://pytorch.org/) = 0.4
- numpy
- scipy
- matplotlib
- scikit-image
- jupyter

All of them can be installed via `conda` (`anaconda`), e.g.
```
conda install jupyter
```


or create an conda env with all dependencies via environment file

```
conda env create -f environment.yml
```

## Docker image

Alternatively, you can use a Docker image that exposes a Jupyter Notebook with all required dependencies. To build this image ensure you have both [docker](https://www.docker.com/) and  [nvidia-docker](https://github.com/NVIDIA/nvidia-docker) installed, then run

```
nvidia-docker build -t deep-image-prior .
```

After the build you can start the container as

```
nvidia-docker run --rm -it --ipc=host -p 8888:8888 deep-image-prior
```

you will be provided an URL through which you can connect to the Jupyter notebook.

## Google Colab

To run it using Google Colab, click the "Open in Colab" buttom.

