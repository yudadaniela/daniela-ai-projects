# Autoencoder for Image Reconstruction — with Hyperparameter Tuning

## Problem
Built and trained an autoencoder on the MNIST handwritten digit dataset 
to compress images into a lower-dimensional latent representation and 
reconstruct them, then systematically experimented with architecture 
and hyperparameter changes to compare their effect on reconstruction 
quality.

## Tools & Approach
- Python: Keras/TensorFlow
- Dataset: MNIST (60,000 training / 10,000 test images, 28×28 pixels 
  each, normalized to [0,1])
- **Baseline model:** input (784) → encoder (32 neurons, ReLU) → 
  decoder (784, sigmoid), Adam optimizer, binary crossentropy loss, 
  10 epochs
- **Modified model:** added a 256-neuron hidden layer, 20% Dropout to 
  reduce overfitting, switched optimizer to SGD (momentum=0.9), 
  changed loss to mean squared error, and tested different epoch 
  counts (15 vs. 50) and learning rates (0.001 vs. 0.01)
- Saved the trained model and its weights (.h5 format)

## My Contribution
Individual project — built the baseline autoencoder, then independently 
ran a series of controlled comparisons across optimizer, learning rate, 
epoch count, and architecture to isolate what actually drove 
reconstruction quality.

## Key Findings
- **Adam consistently outperformed SGD** — it needed fewer epochs to 
  produce quality reconstructions, since it adapts the learning rate 
  per parameter and incorporates momentum automatically
- **Epoch count was critical with SGD:** at 15 epochs, reconstructed 
  images looked like static noise; at 50 epochs, quality improved 
  significantly
- **Learning rate had a similar effect:** 0.001 produced noisy, 
  under-trained reconstructions, while 0.01 gave a clear improvement — 
  too low a learning rate prevented SGD from converging properly
- **Adding a 256-neuron hidden layer alone didn't guarantee better 
  results** — final quality was driven mainly by optimizer choice and 
  epoch count, not architecture size
- **The model struggled with visually similar digits** (e.g., 
  reconstructing a 2 as a 3, or a 4 as a 9), due to the heavy 
  compression (784 → 32 values) losing fine detail, compounded by 
  SGD's weaker learning dynamics compared to Adam

## What I'd Do Differently
Test Adam with the added hidden layer and dropout (instead of only 
pairing the architecture change with SGD), to isolate whether the 
architecture change helps once optimizer is no longer a confounding 
factor.

## Course
Deep Learning 
