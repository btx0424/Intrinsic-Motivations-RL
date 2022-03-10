# Intrinsic-Motivations-and-URL

A non-exhuastive collection of research works regarding intrisic motivations and unsupervised RL.

## Why are they useful?

- Extrinsic rewards can sometimes be sparse or very difficult to design, making it hard for the agent to efficiently learn about the environment and how to achieve an objective.

## Papers
1. [Variational Information Maximisation for Intrinsically Motivated Reinforcement Learning, 2015](https://arxiv.org/abs/1509.08731)
	- maximize the MI between an action sequence and the resulting state given the current state
2. [Incentivizing Exploration In Reinforcement Learning With Deep Predictive Models, 2015](https://arxiv.org/abs/1507.00814)
	- reward novelty as measured by (encoded) state prediction error
3. [Curiosity-driven Exploration by Self-supervised Prediction, 2017](https://proceedings.mlr.press/v70/pathak17a/pathak17a.pdf)
	- reward novelty as measured by (encoded) state prediction error
	- learn what is controllabe/relevant through an inverse dynamics model
4. [VIME: Variational Information Maximizing Exploration, 2017](https://arxiv.org/abs/1605.09674)
	- reward the IG (in dynamics model through observing new transitions) using BNN
5. [Surprise-Based Intrinsic Motivation for Deep Reinforcement Learning, 2017](https://arxiv.org/abs/1703.01732)
	- reward the suprise of seeing the state that is transitioned to
6. [Model-Based Active Exploration, 2019]()
	- reward the IG (in dynamics model through observing new transitions) measured by JSD of an ensemble of dynamics model
7. [Large-Scale Study of Curiosity-Driven Learning, 2018](https://arxiv.org/abs/1808.04355)
	- detailed study on practical considerations
8. [Unsupervised Control Through Non-Parametric Discriminative Rewards, 2019](https://openreview.net/forum?id=r1eVMnA9K7)
	- goal-conditioned policy with a "goal achievement reward"
9. [Diversity is All You Need: Learning Skills without a Reward Function, 2019](https://openreview.net/forum?id=SJx63jRqFm)
	- learn distinguishable and diverse skills by learning to infer skill from states
10. [Mutual Information State Intrinsic Control, 2021](https://openreview.net/forum?id=OthEq8I5v1)
	- maximize the MI between surrounding state and agent state
11. [NovelD: A Simple yet Effective Exploration Criterion, 2021](https://openreview.net/forum?id=CYUzpnOkFJp)
	- reward the increase in novelty (measured by RND) to achieve BFS-like exploration
12. [SMiRL: Surprise Minimizing Reinforcement Learning in Unstable Environments, ICLR2021](https://openreview.net/forum?id=cPZOyoDloxl)
	- minimize the state entropy
13. [Information is Power: Intrinsic Control via Information Capture, NeurIPS2021](https://openreview.net/forum?id=MO76tBOz9RL)
	- minimize the state visitation entropy in a partially observable setting
 
## Comparison 
- exploration: **state** means a wide coverage of the state space, **behavior** means meaningful action sequences that lead to some states. 

|         | Motivation  | Dynamics | Model-Free | Scope    | Exploration |
|---------|-------------|----------|------------|----------|-------------|
| ICM[3]     | novelty     | ✅        | ✅          | global   | state       |
| VIME[4]    | information | ✅        | ✅          | global   | state       |
| DIAYN[9]   | skill       | ✅        | ✅          | global   | behavior    |
| MUSIC[10]   | control     | ❌        | ✅          | global   | behavior    |
| NovelID[11] | novelty difference    | ❌        | ✅          | both     | state       |
| SMiRL[12]     | certainty in state  | ✅        | ✅          | episodic | behavior    |
| IC2[13]     | certainty in state visitation  | ✅        | ✅          | episodic | behavior    |
