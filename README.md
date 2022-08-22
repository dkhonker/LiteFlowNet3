# liteflownet3
This is a personal reimplementation of <a href=https://arxiv.org/abs/2007.09319>LiteFlowNet3</a> [1]  using **PyTorch**, which is based on the <a href=https://github.com/lhao0301/pytorch-liteflownet3/> pytorch-liteflownet3</a> implementation of LiteFlowNet3 by `lhao0301`. 

I have trouble in setuping the correlation layer  in the original codes by `lhao0301` .So I rewrote a code about correlation layer.

Should you be making use of this work, please cite the paper accordingly. Also, make sure to adhere to the <a href="https://github.com/twhui/LiteFlowNet3#license-and-citation">licensing terms</a> of the authors.

For the original Caffe version of this work, please see: https://github.com/twhui/LiteFlowNet3
<br />

## setup
The correlation layer is basen on <a href=https://pypi.org/project/spatial-correlation-sampler/>spatial-correlation-sampler</a>.

```
pip install spatial-correlation-sampler
```

## usage

 To run it on your demo pair of images, use the following command. 


```
python run.py
```

`network-sintel.pytorch` is  from <a href="https://drive.google.com/file/d/1vUSEIxXGZa9d2PQ82SG_gbbIUWLNfH50/view?usp=sharing">lhao0301's Google-Drive </a>.`Only sintel-model is supported now`. 

It's tested with pytorch 1.10.0 and cuda-11.3.

**PS:**

As `sniklaus`  said:

I am afraid that I cannot guarantee that this reimplementation is correct. However, it produced results pretty much identical to the implementation of the original authors in the examples that I tried. There are some numerical deviations that stem from differences in the `DownsampleLayer` of Caffe and the `torch.nn.functional.interpolate` function of PyTorch. 

Please feel free to contribute to this repository by submitting issues and pull requests.

## comparison
<p align="center"><img src="comparison/comparison.gif?raw=true" alt="Comparison"></p>

## license
As stated in the <a href="https://github.com/twhui/LiteFlowNet3#license-and-citation">licensing terms</a> of the authors of the paper, their material is provided for research purposes only. Please make sure to further consult their licensing terms.

## references
```
[1]  @inproceedings{hui2020liteflownet3,
  title={LiteFlowNet3: Resolving Correspondence Ambiguity for More Accurate Optical Flow Estimation},
  author={Hui, Tak-Wai and Loy, Chen Change},
  booktitle={European Conference on Computer Vision},
  pages={169--184},
  year={2020},
  organization={Springer}
}
```

## Acknowledgments
Many code of this repo are borrowed from
<a href=https://github.com/lhao0301/pytorch-liteflownet3/>pytorch-liteflownet3</a>  and  <a href=https://github.com/sniklaus/pytorch-liteflownet>pytorch-liteflownet</a>. 
