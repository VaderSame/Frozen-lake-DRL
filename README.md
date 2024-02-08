openAI gynamsium developing and comparing reinforcement learning algorithms 

# Frozen Lake Environment

## Action Space

- Discrete(4)

## Observation Space

- Discrete(16)

## Description

The Frozen Lake environment involves crossing a frozen lake from start to goal without falling into any holes by walking over the frozen lake. The player may not always move in the intended direction due to the slippery nature of the frozen lake.

## Python Code

```python
import gym

# Creating the Frozen Lake environment
env = gym.make("FrozenLake-v1")

# Arguments for creating the environment
desc = None  # Used to specify non-preloaded maps
map_name = "4x4"  # Default map size
is_slippery = True  # Whether the environment is slippery

# Creating the environment with custom arguments
env_custom = gym.make('FrozenLake-v1', desc=desc, map_name=map_name, is_slippery=is_slippery)

# Specifying a custom map
custom_map = [
    "SFFF",
    "FHFH",
    "FFFH",
    "HFFG"
]
env_custom_custom_map = gym.make('FrozenLake-v1', desc=custom_map)

# Generating a random map
from gym.envs.toy_text.frozen_lake import generate_random_map
random_map = generate_random_map(size=8)
env_random_map = gym.make('FrozenLake-v1', desc=random_map)
