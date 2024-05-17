
# Behavioral Cloning Self-Driving Car
## Introduction

The goal of this project is to develop a self-driving car model using behavioral cloning. The model learns to drive in a simulator by imitating human driving behavior captured in training data. This approach involves collecting driving data, training a deep neural network to predict steering angles from camera images, and then using this network to drive the car autonomously in the simulator.
Dataset Collection

The training data consists of images captured from the car's cameras and corresponding steering angles.
Data is collected by manually driving the car in the simulator and recording the camera images and steering angles.

## Data Preprocessing

Images are preprocessed to remove unnecessary parts (e.g., the hood of the car, areas past the horizon) and resized to reduce training time.
Data augmentation techniques are applied to increase the diversity of the training data and improve the model's generalization.

## Model Architecture

The model architecture consists of convolutional and max-pooling layers followed by fully connected layers.
Activation functions such as PReLU are used to introduce non-linearity, and batch normalization is applied to speed up training and improve convergence.
Dropout layers are used for regularization to prevent overfitting.

## Training Process

The model is trained using the Adam optimizer and mean squared error loss function.
Training is performed over multiple epochs, with the model learning to predict steering angles from the camera images.
The model's performance is evaluated on a separate validation dataset to ensure that it generalizes well to unseen data.

## Results

The trained model is capable of driving the car autonomously in the simulator, following the road and making appropriate steering adjustments based on the input images.
The model's performance is evaluated based on its ability to stay on the road and respond to various driving conditions (e.g., curves, obstacles).

## Conclusion

Behavioral cloning is a promising approach for developing self-driving car models, as it allows the model to learn from human driving behavior. By training a deep neural network on a large dataset of driving data, the model can learn to drive autonomously in a simulator, demonstrating the potential of this approach for real-world applications.


## Source Code
[GitHub Repository](https://github.com/Tinker-Twins/Behavioral-Cloning-Simulator)

## Setup
1. Download and install Unity 5.5.1f1.
2. Clone the repository:
   ```bash
   git clone https://github.com/Tinker-Twins/Behavioral-Cloning-Simulator.git

    Launch Unity and open the project by selecting the parent folder of the cloned repository.

## Usage

 
### Recording Dataset:

    Select the track (Lake Track or Mountain Track).
    Choose Training Mode.
    Click the Record button first time to select the directory to store the recorded dataset.
    Click the Record button second time to start recording the dataset.
    Drive the vehicle manually (check Controls button in Main Menu for manual controls).
    Click the Recording button to stop recording the dataset. The button will show recording progress.

### Training:

    Define a training pipeline to clone human driving behavior based on the recorded dataset.
    Train a deep neural network model to predict control commands based on live camera feed.
    Save the trained model (e.g., H5 file).

### Deployment:

    Define a script to communicate with the simulator using the WebSocket parameters:
        IP Address: 127.0.0.1 (Loopback IP)
        Port Number: 4567
    Develop a deployment pipeline to generate control commands for the autonomous vehicle using the trained model and/or control algorithm.
    Launch the simulator and run the deployment script.

### Data Logging:

    Use the Generate Driving Log button in Training Mode and/or Deployment Mode to log data like Vehicle Position, Throttle Command, Brake Command, Steering Command, and Vehicle Speed within Unity Editor.


### Acknowledgement

This simulator is based on Udacity's Self-Driving Car Simulator.

### Demo

This simulator was used in benchmarking research on Robust Behavioral Cloning for Autonomous Vehicles. Video demonstrations are available on YouTube.
