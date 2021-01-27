# indian_crossroads

Indian crossroads is a Python project for traffic control solution.
The project contains three jupyter notebooks:
Actor_critic.ipynb contains the Neural Network model used for training the agent.
Environment.ipynb contains the Environment used for training the agent.
Agent.ipynb contains the training function for the Actor critic algorithm.

The algorithm used for training is Actor critic. The state space and the action space are continous. 
The Neural Network estimates the parameters alpha and beta for a Beta distribution, from which the algorithm samples, in order to pick an action pair.
The actions the agent can take for each of the four cars are acceleration and curvature.
Both accelerationa and curvature are capped in the (0,1) range.
The Neural Network also estimates the sign with which the agent would take the acceleration (negative sign means the agent will decelerate the velocity of a certain car).



## Usage

Clone the repo locally, and execute the code in the Environment.ipynb and Actor_critic.ipynb notebooks.
After that you can execute the code in the Agent.ipynb, as it imports the classes "Actor_Critic" and "Square_Crossroads".

Modify the hyperparameters and the rewards in the Square_Crossroads class to check how this affects the training.

**NB!** The training procedure is heavily dependant on the hyperparamters and the rewards in the Environment, which makes the training procedure prone to fluctuations.
**NB2!** The deep neural network library used is **Pytorch**

To install the latest version of Pytorch, run:

```bash
pip install torch
```

## License
[MIT](https://choosealicense.com/licenses/mit/)