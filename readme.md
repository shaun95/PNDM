# Pseudo Numerical Methods for Diffusion Models on Manifolds (PNDM)
Luping Liu, Yi Ren, Zhijie Lin, Zhou Zhao

## How to run the code

### Dependencies
Run the following to install a subset of necessary python packages for our code.
```bash
pip install -r requirements.txt
```

### Usage
Train and evaluate our models through main.py.
```bash
python main.py --runner sample --method F-PNDM --sample_step 50 --device cuda --config ddim-cifar10.yml --image_path temp/results --model_path temp/models/ddim/ema_cifar10.ckpt
```
- runner (train|sample): choose the mode of runner 
- method (DDIM|S-PNDM|F-PNDM): choose the numerical methods
- sample_step: choose the total generation step
- device (cpu|cuda:0): choose the device to use
- config: choose the config file
- image_path: choose the path to save images
- model_path: choose the path of model

## Pretrained checkpoints
All checkpoints of models and precalculated statistics for FID are provided in this [Onedrive](https://zjueducn-my.sharepoint.com/:f:/g/personal/3170105432_zju_edu_cn/EhjaZe0ZhnxOrPvejWp0f-cBv8F0xOL9J8xaVyor0fLZEA).

## References
If you find the code useful for your research, please consider citing:
```
@inproceedings{
    liu2022pseudo,
    title={Pseudo Numerical Methods for Diffusion Models on Manifolds},
    author={Luping Liu and Yi Ren and Zhijie Lin and Zhou Zhao},
    booktitle={International Conference on Learning Representations},
    year={2022},
    url={https://openreview.net/forum?id=PlKWVd2yBkY}
}
```
This work is built upon some previous papers which might also interest you:
- Jonathan Ho, Ajay Jain, and Pieter Abbeel. Denoising diffusion probabilistic models. arXiv, 256, 2020.
- Jiaming Song, Chenlin Meng, and Stefano Ermon. Denoising Diffusion Implicit Models. arXiv preprint, pp. 1–19, 2020a.
- Yang Song, Jascha Sohl-Dickstein, Diederik P. Kingma, Abhishek Kumar, Stefano Ermon, and Ben Poole. Score-Based Generative Modeling through Stochastic Differential Equations. pp. 1–32, 2020b.
