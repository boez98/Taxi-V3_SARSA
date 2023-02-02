# Taxi-V3_SARSA
Reinforcement Learning Taxi V3 using SARSA

SARSA algorithm is a slight variation of the popular Q-Learning algorithm. For a learning agent in any Reinforcement Learning algorithm it’s policy can be of two types:

- On Policy: the learning agent learns the value function according to the current action derived from the policy currently being used. 
- Off Policy: the learning agent learns the value function according to the action derived from another policy. 


Q-Learning technique is an Off Policy technique and uses the greedy approach to learn the Q-value. SARSA technique, on the other hand, is an On Policy and uses the action performed by the current policy to learn the Q-value.
The equation for SARSA depends on the current state, current action, reward obtained, next state and next action. SARSA stands for State Action Reward State Action which symbolizes the tuple (s, a, r, s’, a’).


The equation for SARSA depends on the current state, current action, reward obtained, next state and next action.

    Q(s_t,a_t) = Q(s_t,a_t) + alpha* ( r_(t+1) + gamma* Q(s_(t+1),a_(t+1)) - Q(s_t,a_t) )


Where:

- ϵ (epsilon) is the paramenter which choose between exploration (choosing a random action) and exploitation (choosing actions based on already learned Q-values). 

- α (alpha) is the learning rate, it is the extent to which our Q-values are being updated in every iteration.

- γ (gamma) is the discount factor  determines how much importance we want to give to future rewards. A high value for the discount factor (close to 1) captures the long-term effective award, insted a discount factor of 0 makes our agent consider only immediate reward (greedy).



# Result
The program should run for hundreds/thousands of episodes (many hours) to learn and have good result, so I will attach some results.

At the beginning we have pure exploration, the agent will explore every situation making a lot of mistakes.

    Episode:  1
    Goal reached:  0
    Score:  -415

After 100 episodes we are in a 50/50 between exploration and explotation, due to the decreasing value of epsilon. The agent is still learning but it's possible to reach some goal with big negative score.

    Episode:  100
    Goal reached:  0
    Score:  -325

After 200 episodes we can see that the agent is still making mistakes but it start to reach some goals more frequently. Now, we are in pure explotation, the agent should have learned enough to take good decision.

    Episode:  200
    Goal reached:  21
    Score:  -118

We see that in the following next 100 episode (201 to 300) it reached the goal more often.

    Episode:  300
    Goal reached:  92
    Score:  -31

Then, after 400 episodes and more the agent knows perfectly how to interact in every situation taking the best action and the shortest way to reach the goal. It's rare that he doesn't reach the goal.

    Episode:  401
    Goal reached:  182
    Score:  -2

    Episode:  4000
    Goal reached:  3779
    Score:  10
