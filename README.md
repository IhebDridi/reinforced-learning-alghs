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

### Epsilon-Greedy implementation: 
The Epsilon-Greedy algorithm is a simple algorithm that balances exploration and exploitation in a multi-armed bandit problem. Here's a step-by-step guide on how to implement it:

    Initialize a list of N arms, each with an unknown reward probability.

    Set a value for epsilon, which represents the probability of exploration. For example, if epsilon = 0.1, then 10% of the time we will explore a random arm, and 90% of the time we will choose the arm with the highest estimated reward.

    For each round or iteration:
    a. With probability epsilon, choose a random arm to explore.
    b. Otherwise, choose the arm with the highest estimated reward.
    c. Observe the reward from the chosen arm.
    d. Update the estimated reward for the chosen arm based on the observed reward.

    Repeat step 3 for a fixed number of rounds or until convergence.

Here are some variables you will need to use:

    N: the number of arms
    epsilon: the probability of exploration
    Q: a list of length N to store the estimated reward for each arm
    N_pulls: a list of length N to store the number of times each arm has been pulled
    a function to calculate the average reward for each arm

To implement step 3d, you will need to update the estimated reward for the chosen arm using the following formula:
Q[a] = Q[a] + (r - Q[a]) / N_pulls[a]

where a is the index of the chosen arm, r is the observed reward, and N_pulls[a] is the number of times the arm has been pulled before.