# Diffusion
Implemented Denoising Diffusion Probabilistic Model using Pytorch on the CIFAR - 10 Dataset. The model trains well on the dataset as implied by the training and validation loss are almost equal. Hence, the model is neither overfitting nor underfitting. However, the model is not able to generate good quality images. A few reasons for this could be that the dataset is not too huge, the quality of the images are low, the model did not train for a long time and the hyperparameters are not optimized. But it does a fair amount of good amount generation.
______________________________________________________________________________________________________________________________________________________________________________________________

# Possible Improvements
### Loss Function:
  - [ ] Variational Lower Bound (ELBO)
  - [ ] `Simplified ELBO`
  - [ ] `Contrastive Learning Loss Functions: InfoNCE loss`
  - [ ] `Perceptual Loss`

### Optimizers
  - [ ] `Adam with EMA`
  - [ ] `RMSprop`
  - [ ] `RAdam`
  - [ ] `AdaBelief`

### Learning Rate
  Try different values between the range of 1e-5 to 2e-4

### Decay Factor (EMA)
  - [ ] `0.999`
        
    It is a high value that gives a large weight to the previous parameters and a small weight to the current parameters. This can smooth out the fluctuations and noise in the parameter updates, and make the model converge to a better local optimum. However, it may also make the model slow to adapt to new data and prone to overfitting.
  - [ ] `0.9`
        
    This is a lower value that gives a smaller weight to the previous parameters and a larger weight to the current parameters. This can make the model more responsive to new data and less likely to overfit. However, it may also make the model more sensitive to fluctuations and noise in the parameter updates, and less stable in convergence.
  - [ ] `0.5`
        
    This is an even lower value that gives equal weight to the previous parameters and the current parameters. This can make the model balance between smoothing and responsiveness, and achieve a trade-off between stability and adaptability. However, it may also make the model lose some information from the previous parameters and miss some opportunities for improvement.

### Schedules
  - [ ] `Exponential`
  - [ ] `New Learning Rate Scheduler`
    
    A scheduler specifically designed to improve DDPMs.
