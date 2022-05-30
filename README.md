# testmarkdown

### Q1: What is Reinforcement Learning?

<details>
<summary>SOLUTION</summary>
  
Reinforcement learning is a framework for solving control tasks (also called decision problems) by building agents that learn from the environment by interacting with it through trial and error and receiving rewards (positive or negative) as unique feedback

📖: https://huggingface.co/blog/deep-rl-intro#a-formal-definition
  
</details>

### Q2: Define the RL Loop

At every timestep:
- Our Agent receives _______ from the environment
- Based on that _______ the agent takes _________
- Our agent will move to the right
- 

Define the RL Loop:

  Our Agent receives state S_0S 
0
​
  from the Environment — we receive the first frame of our game (Environment).
Based on that state S_0S 
0
​
 , the Agent takes action A_0A 
0
​
  — our Agent will move to the right.
Environment goes to a new state S_1S 
1
​
  — new frame.
The environment gives some reward R_1R 
1
​
  to the Agent — we’re not dead (Positive Reward +1).
<details>
<summary></summary>
  
Reinforcement learning is a framework for solving control tasks (also called decision problems) by building agents that learn from the environment by interacting with it through trial and error and receiving rewards (positive or negative) as unique feedback

  
</details>





<details>
<summary>What's the difference between a state and an observation?</summary>
  
- *The state* is a **complete description of the state of the world** (there is no hidden information). In a fully observed environment. For instance, in chess game, we receive a state from the environment since we have access to the whole check board information.
  
- *The observation* is a **partial description of the state**. In a partially observed environment. For instance, in Super Mario Bros, we only see a part of the level close to the player, so we receive an observation.

  


</details>

### Q: A task is an instance of a Reinforcement Learning problem. What are the two types of tasks?
<details>
<summary>Solution</summary>
-  *Episodic task* : we have a **starting point and an ending point (a terminal state)**. This creates an episode: a list of States, Actions, Rewards, and new States. For instance, think about Super Mario Bros: an episode begin at the launch of a new Mario Level and ending when you’re killed or you reached the end of the level.
  
- *Continous task* : these are tasks that **continue forever (no terminal state)**. In this case, the agent must learn how to choose the best actions and simultaneously interact with the environment.
  
📖: https://huggingface.co/blog/deep-rl-intro#type-of-tasks

</details>

### Q: What is the exploration/exploitation tradeoff?

<details>
<summary>Solution</summary>
  
In Reinforcement Learning, we need to **balance how much we explore the environment and how much we exploit what we know about the environment**. 

- *Exploration* is exploring the environment by **trying random actions in order to find more information about the environment**.

- *Exploitation* is **exploiting known information to maximize the reward**.

📖: https://huggingface.co/blog/deep-rl-intro#exploration-exploitation-tradeoff
</details>

### Q: What are value-based methods?
- Value-based methods is one of the main approaches for solving RL problems.
- In Value-based methods, instead of training a policy function, we train a value function that maps a state to the expected value of being at that state.

📖: https://huggingface.co/blog/deep-rl-intro#value-based-methods



### A small recap of this Unit

That was a lot of information, if we summarize:

Reinforcement Learning is a computational approach of learning from action. We build an agent that learns from the environment by interacting with it through trial and error and receiving rewards (negative or positive) as feedback.

The goal of any RL agent is to maximize its expected cumulative reward (also called expected return) because RL is based on the reward hypothesis, which is that all goals can be described as the maximization of the expected cumulative reward.

The RL process is a loop that outputs a sequence of state, action, reward and next state.

To calculate the expected cumulative reward (expected return), we discount the rewards: the rewards that come sooner (at the beginning of the game) are more probable to happen since they are more predictable than the long term future reward.

To solve an RL problem, you want to find an optimal policy, the policy is the “brain” of your AI that will tell us what action to take given a state. The optimal one is the one who gives you the actions that max the expected return.

There are two ways to find your optimal policy:

By training your policy directly: policy-based methods.
By training a value function that tells us the expected return the agent will get at each state and use this function to define our policy: value-based methods.
Finally, we speak about Deep RL because we introduces deep neural networks to estimate the action to take (policy-based) or to estimate the value of a state (value-based) hence the name “deep.”

