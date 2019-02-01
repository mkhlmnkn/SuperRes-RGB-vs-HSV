# Single Image Super-Resolution (RGB vs HSV)

## Related Works
### SRResNet
* first deep ResNet for SISR
* post-upscaling > pre-upscaling

### EDSR
* using ResBlocks && removing batch-normalization
* increasing features > increasing depth
* residual scaling (x0.1)
* L1-loss (MAE) > L2-loss (MSE)
* geometric self-ensemble
* multi-scale model

### WDSR
* "wide" activation (expand features before ReLU)
* weight normalization instead BN
* global residual pathway + upsampling layer

## Contribution
SISR implementation using HSV image representation. [...]

## Getting Started
* Dataset: [DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/)
* Framework: [TensorFlow](https://www.tensorflow.org/)
* Hardware: [Google Colab](https://colab.research.google.com)

## Used Methods and Architecture
[...]

## Experiments
### Training Details
[...]
### Benchmark Results
[...]

## Conclusion
