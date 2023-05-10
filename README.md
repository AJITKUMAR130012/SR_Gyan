# SRGAN-PyTorch

## Overview

This repository contains an op-for-op PyTorch reimplementation of [Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network](https://arxiv.org/abs/1609.04802v5).


Please refer to `README.md` in the `data` directory for the method of making a dataset.

## How Train and Test

Both training and testing only need to modify the `srgan_config.py` file. 



### Train SRGAN model

- line 41: `mode` change to `train`.

```bash
python3 main.py
```

### Test

Modify the `srgan_config.py` file.

- line 41: `mode` change to `test`.


```bash
python3 test.py
```


## Result

Source of original paper results: [https://arxiv.org/pdf/1609.04802v5.pdf](https://arxiv.org/pdf/1609.04802v5.pdf)

In the following table, the psnr value in `()` indicates the result of the project, and `-` indicates no test.

| Tree images | Scale |       SRGAN        |
|:-----------:|:-----:|:------------------:|
| PSNR        |   4   |  29.40(**30.64**)  |
| SSIM        |   4   |  0.8472(**0.8642**)|


### Result On image
```bash
python3 ./inference.py
```

Input: 

<span align="center"><img width="240" height="360" src="Input/001.jpg"/></span>

Output: 

<span align="center"><img width="240" height="360" src="Output/out1.jpg"/></span>


```
