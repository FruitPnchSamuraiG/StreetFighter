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
- https://github.com/FruitPnchSamuraiG/StreetFighter/1.gif

## Reward Function
- The reward function is set to the in-game score.
- The `step` method reshapes the reward function based on the score delta.

## Training
- Hyperparameters are optimized using Optuna, and the best model is saved.
- The `TrainAndLoggingCallback` class defines a callback to save the model during training.
- The `Train Model` section demonstrates how to train the model using the best hyperparameters.

## Evaluation
- The trained model is evaluated using the `evaluate_policy` function.
- https://github.com/FruitPnchSamuraiG/StreetFighter/2.gif

## Test the Model
- The `Test out the Model` section demonstrates how to use the trained model to play the game.
- https://github.com/FruitPnchSamuraiG/StreetFighter/3.gif

## Files and Directories
- `logs/`: TensorBoard logs during training.
- `opt/`: Saved optimized models.
- `train/`: Checkpoints saved during training.

## Usage
Follow the Jupyter notebook `StreetFighter_Tutorial.ipynb` to understand the code execution flow.


Happy gaming and training!
