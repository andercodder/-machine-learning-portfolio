# Dataset Information

## About the Environment

**Environment**: FrozenLake-v1 (OpenAI Gym)  
**Source**: Standard reinforcement learning benchmark  
**Type**: Simulated grid world environment

## Environment Details

- **State Space**: 100 states (10×10 grid)
- **Action Space**: 4 discrete actions (LEFT, DOWN, RIGHT, UP)
- **Dynamics**: Stochastic transitions (slippery ice)
- **Reward**: +1 for reaching goal, 0 otherwise

## Data Requirements

**No external dataset required!**

This project uses the FrozenLake environment from OpenAI Gym, which is:
- Automatically generated
- Included with the Gym library
- No data files needed

## Running the Notebook

Simply install requirements and run:
```bash
pip install -r requirements.txt
jupyter notebook dqn_frozenlake.ipynb
```

The environment will be created automatically by the code.

---

**Note**: This is a reinforcement learning project using simulated environments, not external datasets.
