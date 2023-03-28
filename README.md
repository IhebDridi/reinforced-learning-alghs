# Reinforced learning algorithms
## Introduction:
There are many types of algorithms that can be used in reinforced learning which can solve many types of problems.

## Multi-armed bandits:
multi-armed bandits are a type of problem in which an agent needs to make a sequence of choices between a set of options, each with an unknown reward.
In reinforcement learning, multi-armed bandits are often used as a simplified model for more complex decision-making problems. The goal of the agent is to maximize its cumulative reward over time, by learning which options have higher rewards and selecting them more often.

The challenge in multi-armed bandits is that the agent must balance exploration (trying out different options to learn about their rewards) and exploitation (selecting the option that is currently believed to have the highest reward). If the agent only exploits what it currently knows, it may miss out on higher rewards from options it hasn't tried yet. On the other hand, if it only explores new options, it may not reap the rewards of the options it already knows to be good.

There are several algorithms that can be used to solve the multi-armed bandit problem, such as epsilon-greedy, UCB (upper confidence bound), and Thompson sampling. These algorithms balance exploration and exploitation in different ways, and can be adapted to different reward structures and assumptions about the environment.

### The Epsilon-Greedy algorithm:
In general, the Epsilon-Greedy algorithm is considered one of the simplest reinforcement learning algorithms to implement, as it only requires a few lines of code and doesn't involve complex mathematical computations.