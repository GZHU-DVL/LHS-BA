# LHS-BA

Code for [Query-Efficient Adversarial Attack Based On Latin Hypercube Sampling] by Dan Wang,  Jiayu Lin, and Yuan-Gen Wang.

## Dependencies
The code for LHS-BA runs with Python and requires Tensorflow of version 1.2.1 or higher. Please `pip install` the following packages:
- `numpy`
- `tensorflow` 
- `keras`
- `scipy`

## Running in Docker, MacOS or Ubuntu
We provide as an example the source code to run LHS-BA on a ResNet trained on CIFAR-10. Run the following commands in shell:

```shell
###############################################
# Omit if already git cloned.
git clone https://github.com/GZHU-DVL/LHS_BA
cd LHS_BA
############################################### 
# Carry out L2 based untargeted attack on 10 iterations.
python main.py --constraint l2 --attack_type untargeted --num_iterations 10
# Carry out L2 based targeted attack on 5 samples.
python main.py --constraint l2 --attack_type targeted --num_iterations 10


# Results are stored in cifar10resnet/figs/.
```

See `main.py` and `LHS_BA.py` for details. 
## Citation
If you use this code for your research, please cite our [paper](https://arxiv.org/abs/2207.02391):
```
@article{wang2022lhsba,
  title={Query-Efficient Adversarial Attack Based On Latin Hypercube Sampling},
  author={Dan Wang,  Jiayu Lin, and Yuan-Gen Wang},
  journal={IEEE International Conference on Image Processing},
  year={2022}
}
```
