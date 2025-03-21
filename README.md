# MambaHSI: Spatial-Spectral Mamba for Hyperspectral Image Classification


<div align="center">
<a href='https://ieeexplore.ieee.org/abstract/document/10604894'><img src='https://img.shields.io/badge/TGRS-Paper-blue'></a>

</div>

## 📝 Introduction
<div align="center">
<img src="./images/Motivation.png" alt="Motivation" width="55%">
</div>

* To our best knowledge, the MambaHSI is **the first image-level hyperspectral image classification model based on SSM**, which can simultaneously model long-range interaction of whole image and integrate spatial and spectral image information.
* MambaHSI demonstrates **the great potential of Mamba to be the next-generation backbone for hyperspectral image models**.

## 🚀 Getting Started

### Installation

```sh
conda create -n MambaHSI_env python=3.9
conda activate MambaHSI_env
conda install pytorch==1.13.1 torchvision==0.14.1 torchaudio==0.13.1 pytorch-cuda=11.7 -c pytorch -c nvidia
pip install packaging==24.0
pip install triton==2.2.0
pip install mamba-ssm==1.2.0
pip install spectral
pip install scikit-learn==1.4.1.post1
pip install calflops==0.3.2
```

### Data Preparation
The dataset can download [Google Drive](https://drive.google.com/file/d/1d-fzMXYhpwis9o_x8hPz4uHx0z5tg7LD/view?usp=sharing) and [BaiduNetdisk](https://pan.baidu.com/s/1SqzP-Y6mbuR1PRz9uGGp1Q?pwd=8ne2).

```
data
└── UP/
    ├── PaviaU.mat 
    └── PaviaU_gt.mat
    ...
└── Houston/
    ├── Houston.mat 
    └── Houston_GT.mat
    ...
└── HanChuan/
    ├── WHU_Hi_HanChuan.mat 
    └── WHU_Hi_HanChuan_gt.mat
    ...
└── HongHu/  
    ├── WHU_Hi_HongHu.npy
    └── WHU_Hi_HongHu_gt.npy
```



**Training:**
```
python train_MambaHSI.py --dataset_index 0
python train_MambaHSI.py --dataset_index 1
python train_MambaHSI.py --dataset_index 2
python train_MambaHSI.py --dataset_index 3
```

## 🎖️ Main Results
<details open>
<summary><font size="4">
Pavia University Results
</font></summary>
<img src="./images/PaviaU_results.png" alt="PaviaU" width="100%">
</details>

<details open>
<summary><font size="4">
Houston Results
</font></summary>
<img src="./images/Houston_results.png" alt="Houston" width="100%">
</details>

<details open>
<summary><font size="4">
HanChuan Results
</font></summary>
<img src="./images/HanChuan_results.png" alt="HanChuan" width="100%">
</details>

<details open>
<summary><font size="4">
HongHu Results
</font></summary>
<img src="./images/HongHu_results.png" alt="HongHu" width="100%">
</details>
