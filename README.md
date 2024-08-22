# multivariable-linear-regression_neural-network
This project is aiming for predicting car price based on given dataset by linear regression using neural network. 

As a continue version of multivariable linear regression, I use neural network here to predict car price. 

# 1. neural network structure. 
For this project, I set 7 layer neural network, 4 of them are nn.Linear(), 3 of them are using nn.ReLu() because data is not perfectly linear. 

# 2. find optimal learning rate. 
Here, I use loop to find the best learning rate to make it neither too large nor too small. Because large learning rate will cause divergent and Oscillation. Too small learning rate will cause slow convergence, underfitting and slow training process issue.
The following picture can demonstrate the issue: 
![image](https://github.com/user-attachments/assets/e9651974-b6d1-4daa-a9e4-73721748f447)
reference: 
https://towardsdatascience.com/https-medium-com-dashingaditya-rakhecha-understanding-learning-rate-dd5da26bb6de

# 3. Main training loop.
For main training loop, I following the basic steps of neural network:
a> do the forward pass.
b> calculate the loss.
c> optimize the zero gradient. 
d> perform backpropagation. 
e> step the optimizer. 
f> test using test set. 

For loss function, I use nn.MSELoss() which is suitable for regression problem. 
For optimizer, I use SGD. Yes, we can use Adam optimizer as well. Most of the cases, both of them perform well. 

# 4. Conclusion.
For this neural network, I get MSE of 0.2 which means 80% accuracy. Since it is a small dataset, I believe neural network is not a proper method. I basically set 10000 epochs to gain this result. 


