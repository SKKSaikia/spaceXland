# SpaceXland  - Landing the Falcon Heavy

🗽✈ [Reinforcement Learning](https://medium.freecodecamp.org/an-introduction-to-reinforcement-learning-4339519de419) to land a SpaceX rocket - Falcon Heavy : in OpenAI [gym](https://github.com/openai/gym#environments) environment

- [Part 1: An introduction to Reinforcement Learning](codecamp.org/an-introduction-to-reinforcement-learning-4339519de419)
- [Part 2: Diving deeper into Reinforcement Learning with Q-Learning](https://medium.freecodecamp.org/diving-deeper-into-reinforcement-learning-with-q-learning-c18d0db58efe)
- [Part 3: An introduction to Deep Q-Learning: let’s play Doom](https://medium.freecodecamp.org/an-introduction-to-deep-q-learning-lets-play-doom-54d02d8017d8)
- [Part 3+: Improvements in Deep Q Learning: Dueling Double DQN, Prioritized Experience Replay, and fixed Q-targets](https://medium.freecodecamp.org/improvements-in-deep-q-learning-dueling-double-dqn-prioritized-experience-replay-and-fixed-58b130cc5682)
- [Part 4: An introduction to Policy Gradients with Doom and Cartpole](https://medium.freecodecamp.org/an-introduction-to-policy-gradients-with-cartpole-and-doom-495b5ef2207f)
- [Part 5: An intro to Advantage Actor Critic methods: let’s play Sonic the Hedgehog!](https://medium.freecodecamp.org/an-intro-to-advantage-actor-critic-methods-lets-play-sonic-the-hedgehog-86d6240171d)
- [Part 6: Proximal Policy Optimization (PPO) with Sonic the Hedgehog 2 and 3]()

# SpaceX OpenAI : [new environment](https://discuss.openai.com/t/new-spacex-openai-gym-environment/3287) -  [The Original Problem](https://github.com/arex18/rocket-lander)

Compared to the [lunar lander](https://gym.openai.com/envs/LunarLander-v2/), it takes magnitudes of more control effort to successfully land the rocket. Besides having a higher center of gravity, the ratio of the force of the side engines to the main engines is much smaller in the rocket, making it impossible to keep upright unless the nozzle is rotated in a controlled way. Then again, the relatively large longitudinal length of the rocket amplifies small changes in the nozzle angle, making it very sensitive and unstable. Welcome to the problem.

<img src="https://github.com/SKKSaikia/spaceXland/blob/master/falcon-heavy.gif">

A basic explanation:
In reinforcement learning we have an agent (The "AI") that is interacting with an environment (The Falcon 9 falling from the sky). It starts knowing absolutely nothing about the environment and tries new things until it gets better at it. It gets feedback about how good some taken action was in the form of a reward. Here, it gets rewarded for slowing down, getting closer to the ship and finally for a nice touchdown. It gets punished for taking too much time, which is equivalent to using too much fuel (a quicker descent without hovering is more efficient). So based on that feedback it will do the things more often that lead to a higher reward and avoid less successful moves. There's randomness in position, linear and angular velocity. Way more than in the real thing of course to make it interesting and more robust.


Siraj Raval did a [PPO implementation](https://github.com/llSourcell/Landing-a-SpaceX-Falcon-Heavy-Rocket) for OpenAI gym environment based on [Unity ML Agents](https://github.com/Unity-Technologies/ml-agents) 
