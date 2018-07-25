Adversarially Regularized Graph Autoencoder (ARGA)
============

This is a TensorFlow implementation of the Adversarially Regularized Graph Autoencoder(ARGA) model as described in our paper:
 
Pan, S., Hu, R., Long, G., Jiang, J., Yao, L., & Zhang, C. (2018). Adversarially Regularized Graph Autoencoder. arXiv preprint arXiv:1802.04407 [https://arxiv.org/abs/1802.04407].

![Construction of ARGA](AGAE_FLOW.pdf)

We borrowed part of code from T. N. Kipf, M. Welling, Variational Graph Auto-Encoders [https://github.com/tkipf/gae]


## Installation

```bash
python setup.py install
```

## Requirements
* TensorFlow (1.0 or later)
* python 2.7
* networkx
* scikit-learn
* scipy

## Run from

```bash
python run.py
```

## Data

In order to use your own data, you have to provide 
* an N by N adjacency matrix (N is the number of nodes), and
* an N by D feature matrix (D is the number of features per node) -- optional

Have a look at the `load_data()` function in `input_data.py` for an example.

In this example, we load citation network data (Cora, Citeseer or Pubmed). The original datasets can be found here: http://linqs.cs.umd.edu/projects/projects/lbc/ and here (in a different format): https://github.com/kimiyoung/planetoid

## Models

You can choose between the following models: 
* `arga_ae`: Graph Auto-Encoder (with GCN encoder)
* `arga_vae`: Variational Graph Auto-Encoder (with GCN encoder)

## Cite

Please cite following papers if you use this code in your own work:

```
@article{pan2018adversarially,
  title={Adversarially Regularized Graph Autoencoder},
  author={Pan, Shirui and Hu, Ruiqi and Long, Guodong and Jiang, Jing and Yao, Lina and Zhang, Chengqi},
  journal={arXiv preprint arXiv:1802.04407},
  year={2018}
}
```
