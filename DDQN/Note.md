# Double DQN

Environment
-----------
Cart Pole

Employed Features
-----------------
- **Expirence Replay**: A vital and standard mechanism in value-based RL.
- **ϵ-Greedy with Decaying ϵ**: A standard solution to the exploration-exploitation problem. It is employed to improve the diversity of the behavior of the agent.
- **Double DQN**: A simple but powerful improvement of vanilla DQN, which can relieve the unstability.

Experiment Notes
----------------
- Since the task (Cart Pole) is very simple, I only employ a very small fully-connected network. Larger networks performed very poorly in the experiment.
- When I used *Sigmoid* as the activation function, the network just broked. It always output the same values no matter what input it got. Currentlu I have no idea why it be like this.
- In my case, the model doesn't work with *L1 loss* (and it's variants) and I chose *MSE* eventually. However, there are many examples on the internet use *L1 loss*. I have no idea what the difference is.
- RL is really very unstable, even for such a simple task. It is exactly an important issue to improve its stability.

References
---------
- Playing Atari with Deep Reinforcement Learning, V. Mnih, 2013.
- Deep Reinforcement Learning with Double Q-learning, H. V. Hasselt, 2015.
