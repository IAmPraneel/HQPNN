# HQPNN
Simulating the Hybrid Quantum-Classical Photonic Neural Network (HQPNN) from Austin et al.

**Reference:**  
Hybrid Quantum-Classical Photonic Neural Networks (arXiv:2407.02366v2 [quant-ph], 14 Jul 2024)  
Tristan Austin, Andrew Hayman, Nir Rotenberg, Simon Bilodeau, Bhavin J. Shastri


 ## Key Features

### 1. Complete Simulation Pipeline
- Prepares synthetic classification datasets with normalization and train/validation/test splits.
- Implements a hybrid neural network architecture: classical pre-encoder → quantum photonic layer → classical post-decoder.
- Quantum layer simulated using **Strawberry Fields (PennyLane interface)** with parameter-shift differentiation.
- Fully compatible with **PyTorch** for end-to-end gradient-based training.

### 2. Flexible Experiment Configuration
- Supports running multiple configurations of qubits, layers, sample sizes, and random seeds.
- Each configuration automatically generates distinct model names and corresponding logs for reproducibility.
- Allows GPU acceleration where available (optional).

### 3. Epoch-wise Logging
- Logs training and validation loss per epoch.
- Tracks total gradient norm and layer-wise gradient norms for detailed diagnostics.
- Saves all metrics in **JSON** and **CSV** formats for post-analysis.

### 4. Reproducibility & Assumptions
- Random seeds are set for Python, NumPy, and PyTorch to ensure deterministic behavior.
- Assumptions are explicitly documented in the code (e.g., quantum encoding of inputs).
- Training hyperparameters, optimizer settings, and learning rate scheduler are configurable.

### 5. Outputs
- Trained model parameters saved as `.pth` files.
- Predictions and labels saved for post-processing.
- Run summaries saved per configuration for easy comparison of model performance across settings.

