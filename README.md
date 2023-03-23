# PaFF
This repository contains the code for the following paper:

**Delving Deep into Pixel Alignment Feature for Accurate Multi-view Human Mesh Recovery**   
Kai Jia, Hongwen Zhang, Liang An, Yebin Liu

AAAI, 2023

### [[Project Page]](https://kairobo.github.io/PaFF/) | [[Paper]](https://arxiv.org/pdf/2301.06020.pdf)
<br/>

[![PaFF](https://Kairobo.github.io/PaFF/assets/overview.png "PaFF")](https://kairobo.github.io/PaFF)

## TODO List 
- [ ] Demo code and pretrained model
- [ ] Code for evaluation
- [ ] Code for training

## Requirements

- Python 3.6.10

### packages

- [PyTorch](https://www.pytorch.org) tested on version 1.1.0

- [torchvision](https://www.pytorch.org) tested on version 0.3.0

- [Neural Renderer](https://github.com/daniilidis-group/neural_renderer) (render densepose labels for training)

- [opendr](https://gitlab.eecs.umich.edu/ngv-python-modules/opendr#) (visualization in training)

- [pyrender](https://github.com/mmatl/pyrender) (optional for demo)

- other packages listed in `requirements.txt`

### necessary files

> mesh_downsampling.npz & DensePose UV data

- Run the following script to fetch mesh_downsampling.npz & DensePose UV data from other repositories.

```
bash fetch_data.sh
```
> SMPL model files

- Collect SMPL model files from [https://smpl.is.tue.mpg.de](https://smpl.is.tue.mpg.de) and [UP](https://github.com/classner/up/blob/master/models/3D/basicModel_neutral_lbs_10_207_0_v1.0.0.pkl). Rename model files and put them into the `./data/smpl` directory.

> Fetch preprocessed data from [SPIN](https://github.com/nkolot/SPIN#fetch-data).

> Download the [pre-trained model](https://drive.google.com/drive/folders/1R4_Vi4TpCQ26-6_b2PhjTBg-nBxZKjz6?usp=sharing) and put it into the `./data/pretrained_model` directory.

After collecting the above necessary files, the directory structure of `./data` is expected as follows.  
```
./data
├── dataset_extras
│   └── .npz files
├── J_regressor_extra.npy
├── J_regressor_h36m.npy
├── mesh_downsampling.npz
├── pretrained_model
│   └── PyMAF_model_checkpoint.pt
├── smpl
│   ├── SMPL_FEMALE.pkl
│   ├── SMPL_MALE.pkl
│   └── SMPL_NEUTRAL.pkl
├── smpl_mean_params.npz
├── static_fits
│   └── .npy files
└── UV_data
    ├── UV_Processed.mat
    └── UV_symmetry_transforms.mat
```