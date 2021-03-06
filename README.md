# Co-teaching
NIPS'18: Co-teaching: Robust Training of Deep Neural Networks with Extremely Noisy Labels (Pytorch implementation).

========

This is the code for the paper:
[Co-teaching: Robust Training of Deep Neural Networks with Extremely Noisy Labels](https://arxiv.org/abs/1804.06872)  
Bo Han, Quanming Yao, Xingrui Yu, Gang Niu, Miao Xu, Weihua Hu, Ivor Tsang, Masashi Sugiyama  
To be presented at [NIPS 2018](https://nips.cc/Conferences/2018/).  

If you find this code useful in your research then please cite  
```bash
@inproceedings{Han2018CoteachingRT,
  title={Co-teaching: Robust Training of Deep Neural Networks with Extremely Noisy Labels},
  author={Bo Han and Quanming Yao and Xingrui Yu and Gang Niu and Miao Xu and Weihua Hu and Ivor W. Tsang and Masashi Sugiyama},
  booktitle={NIPS},
  year={2018}
}
```  

## Setups
All code was developed and tested on a single machine equiped with a NVIDIA K80 GPU. The environment is as bellow:  

- CentOS 7.2
- CUDA 8.0
- Python 2.7.12 (Anaconda 4.1.1 64 bit)
- PyTorch 0.3.0.post4
- numpy 1.14.2

Install PyTorch via:
```bash
pip install http://download.pytorch.org/whl/cu80/torch-0.3.0.post4-cp27-cp27mu-linux_x86_64.whl
```

## Running Co-teaching on benchmark datasets (MNIST, CIFAR-10 and CIFAR-100)
Here is an example: 

```bash
python main.py --dataset cifar10 --noise_type symmetric --noise_rate 0.5 
```

## Performance

| (Flipping, Rate) | MNIST  | CIFAR-10 | CIFAR-100 |
| ---------------: | -----: | -------: | --------: |
| (Pair, 45%)      | 87.58% | 72.85%   | 34.40%    |
| (Symmetry, 50%)  | 91.68% | 74.49%   | 41.23%    |
| (Symmetry, 20%)  | 97.71% | 82.18%   | 54.36%    |



Contact: Xingrui Yu (xingrui.yu@student.uts.edu.au); Bo Han (bo.han@riken.jp).
