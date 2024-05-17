# Behavioral Cloning Simulator

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

### Citation

If you use this simulator for your research, please cite the following paper:


@article{RBCAV-2021,
author = {Samak, Tanmay Vilas and Samak, Chinmay Vilas and Kandhasamy, Sivanathan},
title = {Robust Behavioral Cloning for Autonomous Vehicles Using End-to-End Imitation Learning},
journal = {SAE International Journal of Connected and Automated Vehicles},
volume = {4},
number = {3},
pages = {279-295},
month = {aug},
year = {2021},
doi = {10.4271/12-04-03-0023},
url = {https://doi.org/10.4271/12-04-03-0023},
issn = {2574-0741}
}

### Acknowledgement

This simulator is based on Udacity's Self-Driving Car Simulator.

### Demo

This simulator was used in benchmarking research on Robust Behavioral Cloning for Autonomous Vehicles. Video demonstrations are available on YouTube.
