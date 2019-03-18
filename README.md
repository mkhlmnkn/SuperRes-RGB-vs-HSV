# Single Image Super-Resolution (RGB vs HSV)

## Abstract
*abstract text*

## Related Works
### [SRResNet](https://arxiv.org/abs/1609.04802)
* first deep ResNet for SISR
* post-upscaling > pre-upscaling

### [EDSR](https://arxiv.org/abs/1707.02921)
* using ResBlocks && removing batch-normalization
* increasing features > increasing depth
* residual scaling (x0.1)
* L1-loss (MAE) > L2-loss (MSE)
* geometric self-ensemble
* multi-scale model

### [WDSR](https://arxiv.org/abs/1808.08718)
* "wide" activation (expand features before ReLU)
* weight normalization instead BN
* global residual pathway + upsampling layer

## Contribution
* SISR implementation training by HSV image representation
* Comparison of RGB and HSV results

## Getting Started
* Training dataset: [DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/)
* Framework: [TensorFlow](https://www.tensorflow.org/)
* Hardware: [Google Colab](https://colab.research.google.com)

## Training
### Architecture
<p align="center">
  <img src="https://raw.githubusercontent.com/mkhlmnkn/SuperRes-RGB-vs-HSV/master/images/for%20readme/edsr%20arch%20.png" alt="EDSR"/>
</p>

### Parameters
* Kernel size: <!--5\times5-->
* Number of feature maps (for res blocks): 32
* Сoefficient of residual scaling: 0.1
* Number of residual blocks: 16
* Adam Optimizer
* Learning rate: <!--10^{-5}-->
* L2 regularization сoefficient: <!--10^{-2}-->

## Benchmark Results
### Loss
Counted the loss for any step such that step $\equiv$ 0 images (mod 25)
<p align="center">
  <img src="https://raw.githubusercontent.com/mkhlmnkn/SuperRes-RGB-vs-HSV/master/images/for%20readme/loss.png" alt="Loss"/>
</p>

### DIV2K 0809
<p align="center">
  <img src="https://raw.githubusercontent.com/mkhlmnkn/SuperRes-RGB-vs-HSV/master/images/for%20readme/0809.png" alt="0809"/>
</p>

### DIV2K 0841
<p align="center">
  <img src="https://raw.githubusercontent.com/mkhlmnkn/SuperRes-RGB-vs-HSV/master/images/for%20readme/0841.png" alt="0841"/>
</p>

### DIV2K 0853
<p align="center">
  <img src="https://raw.githubusercontent.com/mkhlmnkn/SuperRes-RGB-vs-HSV/master/images/for%20readme/0853.png" alt="0853"/>
</p>

## Conclusion
Underfitting! Need more epoches.
