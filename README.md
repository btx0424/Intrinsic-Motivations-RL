# Intrinsic-Motivations-and-URL
This repo collects notable works on intrisic motivations in RL and unsupervised RL.

IG: Information gain
MI: Mutual Information
- [Variational Information Maximisation for Intrinsically Motivated Reinforcement Learning, 2015](https://arxiv.org/abs/1509.08731)
	- maximize the MI between an action sequence and the resulting state given the current state
- [Incentivizing Exploration In Reinforcement Learning With Deep Predictive Models, 2015](https://arxiv.org/abs/1507.00814)
	- reward novelty as measured by (encoded) state prediction error
- [Curiosity-driven Exploration by Self-supervised Prediction, 2017](https://proceedings.mlr.press/v70/pathak17a/pathak17a.pdf)
	- reward novelty as measured by (encoded) state prediction error
	- learn what is controllabe/relevant through an inverse dynamics model
- [VIME: Variational Information Maximizing Exploration, 2017](https://arxiv.org/abs/1605.09674)
	- reward the IG (in dynamics model through observing new transitions) using BNN
- [Surprise-Based Intrinsic Motivation for Deep Reinforcement Learning, 2017](https://arxiv.org/abs/1703.01732)
	- reward the suprise of seeing the state that is transitioned to
- [Model-Based Active Exploration, 2019]()
	- reward the IG (in dynamics model through observing new transitions) measured by JSD of an ensemble of dynamics model
- [Large-Scale Study of Curiosity-Driven Learning, 2018](https://arxiv.org/abs/1808.04355)
	- detailed study on practical considerations
- [Unsupervised Control Through Non-Parametric Discriminative Rewards, 2019](https://openreview.net/forum?id=r1eVMnA9K7)
	- goal-conditioned policy with a "goal achievement reward"
- [Diversity is All You Need: Learning Skills without a Reward Function, 2019](https://openreview.net/forum?id=SJx63jRqFm)
	- learn distinguishable and diverse skills by learning to infer skill from states
- [Mutual Information State Intrinsic Control, 2021](https://openreview.net/forum?id=OthEq8I5v1)
	- maximize the MI between surrounding state and agent state
- [NovelD: A Simple yet Effective Exploration Criterion, 2021](https://openreview.net/forum?id=CYUzpnOkFJp)
	- reward the increase in novelty (measured by RND) to achieve BFS-like exploration
- [Information is Power: Intrinsic Control via Information Capture](https://openreview.net/forum?id=MO76tBOz9RL)
	- minimize the state visitation entropy
