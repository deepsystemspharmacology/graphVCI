# Graph Variational Causal Inference

https://arxiv.org/pdf/2210.00116.pdf

This repository implements Graph Variational Causal Inference (graphVCI), a framework that integrates pre-trained relational information into variational causal inference for the prediction and estimation of perturbation effect on gene expressions at single-cell and marginal level.


## Installation

### 1. Create Conda Environment
```bash
conda config --append channels conda-forge
conda create -n gvci-env --file requirements.txt
conda activate gvci-env
```

### 2. Install Learning Libraries
- [Pytorch](https://pytorch.org/) [**1.11**.0](https://pytorch.org/get-started/previous-versions/)
- [Pytorch Geometric](https://pytorch-geometric.readthedocs.io/en/latest/) [**2.0**.4](https://pytorch-geometric.readthedocs.io/en/2.0.4/notes/installation.html)

  \* *make sure to install the right versions for your toolkit*

### 3. Install Submodule
```bash
git submodule update --init --recursive
pip install -e variational-causal-inference
```


## Run
Once the environment is set up, the function call to train & evaluate graphVCI is:

```bash
./main_train.sh &
```

A list of flags may be found in `main_train.sh` and `src/main_train.py` for experimentation with different network parameters. The run log and models are saved under `*artifact_path*/saves`, and the tensorboard log is saved under `*artifact_path*/runs`.

## License

Contributions are welcome! All content here is licensed under the MIT license.
