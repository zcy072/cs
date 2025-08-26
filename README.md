# 📖 HAFRSR

### HAFRSR: hierarchical attention and feature re-aggregation network for lightweight image super-resolution



## 📄 Related Publication

This code is directly associated with our manuscript currently under review at **The Visual Computer** journal:

> **HAFRSR: Enhancing Lightweight Image Super-Resolution through Hierarchical Attention and Feature Re-aggregation** 
> Authors: Chuangye Zhao, Yitao Liang, Jiale Wang, Degang Xu, Bin Li, Juan Xia  
> Status: Under Review at The Visual Computer  
> Submission ID: 0afe6f20-0dfd-4930-8d3a-b9d791af1554

**If you use this code in your research, please consider citing our work once published.**

## 🔗 Code Availability Statement

This repository provides the complete implementation of HAFRSR, including:

- Dependencies and requirements
- Training and evaluation scripts  
- Pre-trained models
- Detailed usage documentation

The code is made available to support reproducibility and enable researchers to replicate our experimental results as described in the manuscript.



## Environment

**Recommend using tools similar to Miniconda for environment management.**

- Platforms: Ubuntu, CUDA >= 11.8
- [Python >= 3.10](https://www.python.org/) (Recommend using [Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main))
- [PyTorch >= 2.3](https://pytorch.org/)
- [BasicSR == 1.4.2](https://github.com/XPixelGroup/BasicSR) **(Recommend using our implementation)**

The environment we use is: `Python == 3.10, Pytorch == 2.3, CUDA == 12.1`

### Installation

```
# Clone the repo
https://github.com/zcy072/HAFASR.git

# Install dependent packages
cd HAFASR
conda create -n hafasr python=3.10
conda activate hafasr

# Install Pytorch (for example)
pip install torch==2.3.0 torchvision==0.18.0

# Install BasicSR
pip install -r requirements.txt
python setup.py develop
```

You can also refer to [this page](https://github.com/XPixelGroup/BasicSR/blob/master/docs/INSTALL.md) for installation.

## Data Preparation

Please refer to [datasets/REDAME.md](datasets/README.md) for data preparation.

## How To Test

- Refer to `./options/test` for the configuration file of the model to be tested, and prepare the testing data and pretrained model.

```
python basicsr/test.py -opt options/test/HAFASR_DF2K_x2SR.yml
```

The testing results will be saved in the `./results` folder.

## How To Train

- Refer to `./options/train` for the configuration file of the model to train.

- Preparation of training data can refer to [this page](https://github.com/XPixelGroup/BasicSR/blob/master/docs/DatasetPreparation.md).

  ```
  python basicsr/train.py -opt options/train/HAFASR_DF2K_100w_x2SR.yml
  ```

  More training commands can refer to [this page](https://github.com/XPixelGroup/BasicSR/blob/master/docs/TrainTest.md).

The training logs and weights will be saved in the `./experiments` folder.



## Acknowledgement

This code is based on [BasicSR](https://github.com/XPixelGroup/BasicSR). Thanks for their awesome works.

## Contact

If you have any question, please email zhaocy720@163.com.
