# Kinematics prediction of double pendulum_LSTM
## Introduction
The trajectories of double pendulum are shown below.
<img width="680" alt="image" src="https://github.com/user-attachments/assets/6fba4037-30c6-4cd2-ad3a-1d642b3fee4f">
Using an LSTM approch, the model set with 200 epoches, 64 batch sizs Adam optimiser and MSE as loss function. The loss function tends to be stable as the number of training rounds decreases, indicating that the model's performance on the training set gradually stabilizes, and there is no significant over-fitting or under-fitting. The prediction results of the model basically coincide with the actual data, indicating that the model can learn the dynamics of the double pendulum system well and accurately predict the future positions of m1 and m2.
<img width="581" alt="image" src="https://github.com/user-attachments/assets/e4dba2b4-3b3a-45ec-a799-0cf03ae4b7cc">
<img width="897" alt="image" src="https://github.com/user-attachments/assets/684be39f-06bb-44db-8e6a-22676e161498">

The physical motion of masses would be more complex and chaotic with different initial condition, making it difficult for the model to learn. The model predicts the best results using the initial condition [π/4, 0, π/4, 0], which may mean that the motion of the double pendulum system under this condition is more regular, or the model is easier to capture to the characteristics of this state of motion.
![下载 (3)](https://github.com/user-attachments/assets/e161ad05-0296-437a-aa29-e318641489de)
As shown in the figure above, the prediction errors (RMSE) of y1 and y2 shows a stable performance in long-term prediction. In particular, the x1 and x2 error first increases and then decreases after increasing the prediction time.
![下载 (7)](https://github.com/user-attachments/assets/f6c2f54a-1288-4610-9b31-79f5c7bc6607)

Using only the information from lower mass, training puts higher requirements on the generalization ability of the model and the depth of understanding of complex systems. How well a model performs will reflect its ability to capture the core dynamics of the system. However, due to the lack of position information of mass m1, the prediction accuracy of the model may be reduced, especially in long-term predictions and complex initial conditions.
![下载 (8)](https://github.com/user-attachments/assets/7abfcbf1-5f87-4bfb-800a-31c08cfe0329)

