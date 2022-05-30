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
