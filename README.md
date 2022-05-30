# testmarkdown

### Q1: What is Reinforcement Learning?

<details>
<summary>Solution</summary>
  
Reinforcement learning is a framework for solving control tasks (also called decision problems) by building agents that learn from the environment by interacting with it through trial and error and receiving rewards (positive or negative) as unique feedback

📖: https://huggingface.co/blog/deep-rl-intro#a-formal-definition
  
</details>

### Q2: Define the RL Loop

<img src="assets/img/rl-loop-ex" alt="Exercise RL Loop"/>

At every step:
- Our Agent receives ______ from the environment
- Based on that ______ the agent takes an ______
- Our agent will move to the right
- The Environment goes to a ______
- The Environment gives ______ to the agent

<details>
<summary>Solution</summary>

<img src="assets/img/rl-loop-solution" alt="Exercise RL Solution"/>
  

At every step:
- Our Agent receives **state s0** from the environment
- Based on that **state s0** the agent takes an **action a0**
- Our agent will move to the right
- The Environment goes to a **new state s1**
- The Environment gives **a reward r1** to the agent

<details>
<summary></summary>
  
Reinforcement learning is a framework for solving control tasks (also called decision problems) by building agents that learn from the environment by interacting with it through trial and error and receiving rewards (positive or negative) as unique feedback

  
</details>





<details>
<summary>What's the difference between a state and an observation?</summary>
  
- *The state* is a **complete description of the state of the world** (there is no hidden information). In a fully observed environment. For instance, in chess game, we receive a state from the environment since we have access to the whole check board information.
  
- *The observation* is a **partial description of the state**. In a partially observed environment. For instance, in Super Mario Bros, we only see a part of the level close to the player, so we receive an observation.

  


</details>

### Q3: A task is an instance of a Reinforcement Learning problem. What are the two types of tasks?
<details>
<summary>Solution</summary>
-  *Episodic task* : we have a **starting point and an ending point (a terminal state)**. This creates an episode: a list of States, Actions, Rewards, and new States. For instance, think about Super Mario Bros: an episode begin at the launch of a new Mario Level and ending when you’re killed or you reached the end of the level.
  
- *Continous task* : these are tasks that **continue forever (no terminal state)**. In this case, the agent must learn how to choose the best actions and simultaneously interact with the environment.
  
📖: https://huggingface.co/blog/deep-rl-intro#type-of-tasks

</details>

### Q4: What is the exploration/exploitation tradeoff?

<details>
<summary>Solution</summary>
  
In Reinforcement Learning, we need to **balance how much we explore the environment and how much we exploit what we know about the environment**. 

- *Exploration* is exploring the environment by **trying random actions in order to find more information about the environment**.

- *Exploitation* is **exploiting known information to maximize the reward**.

📖: https://huggingface.co/blog/deep-rl-intro#exploration-exploitation-tradeoff
</details>

### Q5: What is a policy?

<details>
<summary>Solution</summary>
  
- The Policy π **is the brain of our Agent**, it’s the function that tell us what action to take given the state we are. So it defines the agent’s behavior at a given time.

📖: https://huggingface.co/blog/deep-rl-intro#the-policy-%CF%80-the-agents-brain
</details>


### Q6: What are value-based methods?
- Value-based methods is one of the main approaches for solving RL problems.
- In Value-based methods, instead of training a policy function, we train a value function that maps a state to the expected value of being at that state.

📖: https://huggingface.co/blog/deep-rl-intro#value-based-methods

### Q6: What are policy-based methods?

<details>
<summary>Solution</summary>
  
- In *Policy-Based Methods*, we learn a **policy function directly**.
- This policy function will **map from each state to the best corresponding action at that state**. Or a **probability distribution over the set of possible actions at that state**.

<img src="assets/img/policy.jpg" alt="Policy illustration"/>

📖: 
  

</details>

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

