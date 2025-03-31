The MLPRegressor (Multi-Layer Perceptron Regressor) is created using the ENB2012 dataset. It is a supervised machine learning model that applies a neural network architecture to perform regression. Here’s how it works:
ENB2012 Dataset Overview
The ENB2012 dataset is commonly used for energy efficiency prediction. It contains eight input features related to the physical characteristics of buildings, such as:
- X1: Relative compactness  
- X2: Surface area  
- X3: Wall area  
- X4: Roof area  
- X5: Overall height  
- X6: Orientation  
- X7: Glazing area  
- X8: Glazing area distribution  

The dataset has two target variables:
- Y1: Heating Load  
- Y2: Cooling Load  

The MLPRegressor uses these input features to predict either Y1 or Y2.
How MLPRegressor Works
1. Input Layer: 
   - The model takes the eight building characteristics as input features.  
   - Each feature is assigned a weight, which determines its influence on the output.

2. Hidden Layers: 
   - The MLPRegressor uses one or more hidden layers with neurons, where it applies weighted sums and an activation function (e.g., ReLU or Tanh).  
   - These layers capture non-linear relationships in the data, making the model more effective for complex, non-linear patterns.

3. Activation Function:  
   - Each neuron applies the tanh activation function defined as : f(x)=tanh(x)= (e^x-e^-x)/(e^x+e^-x)
   - The Tanh function produces outputs in the range (-1, 1), which helps:
   - Center the data around zero, making the model more stable.
   - Improve convergence during training by reducing internal covariate shifts.
   - Capture complex, non-linear relationships in the data.

4. Backpropagation and Gradient Descent:
   - During training, the model uses backpropagation to minimize the error between predicted and actual values.  
   - The model adjusts weights using gradient descent, iteratively reducing the loss function (Mean Squared Error, MSE, by default).

5. Output Layer: 
   - The final layer produces a continuous output value, making it suitable for regression tasks like predicting heating and cooling loads.

Why MLP for ENB2012?
- Captures non-linear relationships: 
   - Building characteristics and energy loads have complex dependencies, which MLP handles better than traditional linear regression.  
- High-dimensional data:  
   - With eight features, MLPRegressor efficiently handles the multi-dimensional input space.  
- Regression capabilities:
   - MLP outputs continuous values, making it ideal for predicting energy efficiency metrics.

Final Outcome
Your MLPRegressor learns from the training data and makes predictions on the energy loads (Y1 and Y2), considering the physical features of the building. It estimates heating and cooling requirements accurately by identifying patterns and dependencies between building characteristics and energy consumption.
