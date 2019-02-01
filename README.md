# SuperResolution (RGB vs HSV)
## Related works
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
