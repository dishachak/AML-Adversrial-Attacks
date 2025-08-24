# Adversarial Attacks on Deep Image Classification Models

## Objective
This project investigates the vulnerability of deep convolutional neural networks (CNNs) to adversarial attacks and evaluates defensive distillation as a defense mechanism.

## Dataset
- Tiny ImageNet (200 classes, subset of ImageNet)

## Model
- Pre-trained ResNet34 (PyTorch)
- Baseline accuracy:
  - Top-1: 80.62%
  - Top-5: 95.62%

## Attacks Implemented
### 1. Fast Gradient Sign Method (FGSM)
- White-box evasion attack with imperceptible noise.
- Results:
  - Top-1 error: 93.74%
  - Top-5 error: 60.84%

### 2. Adversarial Patch Attack
- Visible, localized patch applied to images.
- Patch sizes tested: 32×32, 48×48, 64×64.
- Causes targeted misclassification.

## Defense Implemented
### Defensive Distillation
- Teacher-student model framework with temperature scaling.
- Improves robustness to simple attacks but not fully resistant.

## Results
- FGSM and Patch attacks cause major accuracy drop.
- Defensive distillation improves robustness slightly but reduces clean accuracy.
- Teacher model > Student model in accuracy.

## Key Takeaways
- CNNs are highly vulnerable to adversarial examples.
- Defensive distillation is not a complete solution.
- Future work: Adversarial training, robust optimization techniques.

## References
- [Adversarial Attacks on Image Classification Models](https://arxiv.org/abs/2307.02055)
- [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1511.04508)
