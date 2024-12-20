# mknox/bettermdptools

## Getting Started

### About

Bettermdptools is a package designed to help users get started with [gymnasium](https://gymnasium.farama.org/), a maintained fork of OpenAI’s Gym library. 
Bettermdptools includes planning and reinforcement learning algorithms, useful utilities and plots, environment models for blackjack and cartpole, and starter code for working with gymnasium.

### Install 

pip install or git clone bettermdptools.   

```
pip install bettermdptools
```

```
git clone https://github.com/jlm429/bettermdptools
```

Starter code to get up and running on the gymnasium frozen lake environment. See [bettermdptools/notebooks](notebooks/) for more.  

```
import gymnasium as gym
from bettermdptools.algorithms.planner import Planner
from bettermdptools.utils.plots import Plots

# make gym environment 
frozen_lake = gym.make('FrozenLake8x8-v1', render_mode=None)

# run VI
V, V_track, pi = Planner(frozen_lake.P).value_iteration()

#plot state values
size=(8,8)
Plots.values_heat_map(V, "Frozen Lake\nValue Iteration State Values", size)
```

![grid_state_values](https://user-images.githubusercontent.com/10093986/211906047-bc13956b-b8e6-411d-ae68-7a3eb5f2ad32.PNG)

## Contributing

Pull requests are welcome.  

* Fork bettermdptools.
* Create a branch (`git checkout -b branch_name`)
* Commit changes (`git commit -m "Comments"`)
* Push to branch (`git push origin branch_name`)
* Open a pull request