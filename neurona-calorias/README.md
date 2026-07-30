# Single Neuron from Scratch — Calorie Prediction

## Problem
Built a single artificial neuron from scratch (no ML libraries like 
TensorFlow or scikit-learn) to predict calorie content based on fat 
and carbohydrate values, implementing the full gradient descent 
training process manually.

## Tools & Approach
- Python: Pandas & NumPy only — no high-level ML frameworks
- Dataset: 20 food records with fat and carbohydrates as input 
  variables, calories as the target
- Implemented from scratch:
  - Forward pass (weighted sum + bias)
  - Cost function (Mean Squared Error)
  - Partial derivatives for each weight and the bias
  - Gradient descent training loop (50,000 epochs)

## My Contribution
Individual project — full implementation of the neuron and training 
algorithm without relying on pre-built ML libraries.

## Key Findings
- The model converged to an error between 437–438 after 50,000 epochs, 
  with a learning rate of 0.001
- **Learning rate sensitivity was the most important discovery:** a 
  learning rate of 0.001 gave slow but stable learning, while 0.01 
  caused the error to explode to NaN — the steps were too large for 
  the model to converge
- The error plateaued rather than reaching near-zero, most likely due 
  to the small dataset (only 20 records) and limited input variables 
  (fat and carbs alone don't fully explain calorie content — protein 
  content, for example, is missing)

## What I'd Do Differently
Add more input variables (e.g., protein) and expand the dataset beyond 
20 records to see whether the error plateau was caused by data 
limitations rather than the model itself.

## Course
Deep Learning
