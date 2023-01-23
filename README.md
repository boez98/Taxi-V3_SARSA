# Taxi-V3_SARSA
Reinforcement Learning Taxi V3 using SARSA

# Result
The program should run for hundreds/thousands of episodes (many hours) to learn and have good result, so I will attach some results.

At the beginning we have pure exploration, the agent will explore every situation making a lot of mistakes. We can see that in the firts 100 episode it reached the goal only 3 times.

    Episode:  1
    Goal reached:  0
    Score:  -334

    Episode:  100
    Goal reached:  3
    Score:  -307

After 100 episodes we are in a 50/50 between exploration and explotation, due to the decreasing value of epsilon. Here we can see that the agent is still making mistakes but it start to reach some goals.

    Episode:  201
    Goal reached:  26
    Score:  -100

Now, after 200 episodes we are in pure explotation, the agent should have learned enough to take good decision, we see that in the last 100 episode (201 to 302) it reached the goal 74 times but it's not perfect yet.

    Episode:  302
    Goal reached:  100
    Score:  -13

Then, after 400 episodes the agent knows perfectly how to interact in every situation taking the best action and the shortest way to reach the goal. It's rare that he doesn't reach the goal.

    Episode:  403
    Goal reached:  193
    Score:  8

    Episode:  3475
    Goal reached:  3261
    Score:  8
