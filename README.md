# fall-2024-final-project-team-15-1

## Team Members: 
- Jimmy Nguyen (MAE)
- Michael Ramirez (MAE)
- Anurag Gajaria (MAE)
- Jingnan Huang (MAE)

## Abstract:



### What we promised
- Detect a person and focuses on them
- Follow selected person at a set distance
- Detect a gesture and take a picture after 3 seconds
- Upload picture to google drive folder

## Model Training
We trained our gesture detection model using Roboflow because it allows you to train custom models and find the dataset from the Roboflow Universe. According to the tutorial provided by Roboflow, we can also implement our CV models on many devices, including OAK-D camera, and this make sure the models can be deployed to the camera via the ROS2 package.

Here is the performance of our person detection model and gesture detection model:
![image](https://github.com/user-attachments/assets/f9e931e4-7155-4159-9587-ec7f2deeef39)
![image](https://github.com/user-attachments/assets/1798919f-650e-499d-9b65-f6b6e74a6f0f)

## Gesture Detecting and Picture taking
We created a ROS2 Node for the picture taking part. In the Node, We created a callback Timer to receive the prediction from the gesture detection model. Once it detects the "Rock", the robot would stop and take a picture after 3 seconds，and save it to the folder we specified. 

