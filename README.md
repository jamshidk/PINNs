Physics Informed🚀 Neural Networks

Components of a PINN:
Neural Network Architecture:

The neural network in a PINN typically takes as input the spatial and temporal coordinates (or any relevant parameters) and outputs the predicted solution to the PDE.
The architecture of the neural network can vary but often includes multiple layers with activation functions.
Loss Function:

The loss function in a PINN consists of two main components:
Data Fitting Term: This part ensures that the model fits the available data. It measures the difference between the predicted values and the observed data.
Physics-Informed Term: This term enforces the PDE constraints. It involves taking derivatives of the neural network predictions with respect to the input variables and comparing them to the corresponding terms in the PDE.
Total Loss=Data Fitting Loss+Physics-Informed Loss
Handling PDE Constraints:

PINNs utilize automatic differentiation to handle the PDE constraints. The gradients of the neural network outputs with respect to the input variables are computed during the training process.
For example, in a heat equation  ∂𝑢∂𝑡=𝛼∂2𝑢∂𝑥2
 , the terms  ∂𝑢∂𝑡
  and  ∂2𝑢∂𝑥2
  are computed using automatic differentiation and compared to enforce the PDE.
