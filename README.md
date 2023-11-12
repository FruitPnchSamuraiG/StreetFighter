# Street Fighter Reinforcement Learning

This repository contains code for training a reinforcement learning model to play Street Fighter II: Special Champion Edition 
using the Proximal Policy Optimization (PPO) algorithm.

## Setup
Remeber to set up the game from the roms folder using the terminal
To run the code, follow the instructions below:
```bash
pip install gym gym-retro
pip install opencv-python
pip install stable-baselines3[extra] optuna
```

## Environment Setup
- The `StreetFighter` class is implemented as a custom environment using the Gym interface.
- Grayscaling, frame delta, and frame resizing are applied to preprocess observations.


## Filtered Action Setup
- The `StreetFighter` environment uses retro.Actions.FILTERED to filter the action space.
- This helps focus on relevant actions for optimal training.
- Random Sampling of Actions
https://github.com/FruitPnchSamuraiG/StreetFighter/assets/146465657/ace2b2c7-80a2-425f-92ca-359d4d68b3fe

## Reward Function
- The reward function is set to the in-game score.
- The `step` method reshapes the reward function based on the score delta.

## Training
- Hyperparameters are optimized using Optuna, and the best model is saved.
- The `TrainAndLoggingCallback` class defines a callback to save the model during training.
- The `Train Model` section demonstrates how to train the model using the best hyperparameters.

## Evaluation
- The trained model is evaluated using the `evaluate_policy` function.
https://github.com/FruitPnchSamuraiG/StreetFighter/assets/146465657/e934897d-32b6-4078-a48e-ff0d8f5f9bd5

## Test the Model
- The `Test out the Model` section demonstrates how to use the trained model to play the game.
  https://github.com/FruitPnchSamuraiG/StreetFighter/assets/146465657/993db446-9b45-4c58-a13e-7cf36e1952d6

## Files and Directories
- `logs/`: TensorBoard logs during training.
- `opt/`: Saved optimized models.
- `train/`: Checkpoints saved during training.

## Usage
Follow the Jupyter notebook `StreetFighter_Tutorial.ipynb` to understand the code execution flow.


Happy gaming and training!
