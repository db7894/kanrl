# Kolmogorov-Arnold Q-Network (KAQN) - KAN applied to Reinforcement learning, initial experiments

This small project test the novel architecture Kolmogorov-Arnold Networks (KAN) in the reinforcement learning paradigm to the CartPole problem. 

Kolmogorov-Arnold Networks (KANs) are promising alternatives of Multi-Layer Perceptrons (MLPs). KANs have strong mathematical foundations just like MLPs: MLPs are based on the universal approximation theorem, while KANs are based on Kolmogorov-Arnold representation theorem. KANs and MLPs are dual: KANs have activation functions on edges, while MLPs have activation functions on nodes. This simple change makes KANs better (sometimes much better!) than MLPs in terms of both model accuracy and interpretability.

<img width="1163" alt="mlp_kan_compare" src="https://github.com/KindXiaoming/pykan/assets/23551623/695adc2d-0d0b-4e4b-bcff-db2c8070f841">

For more information about this novel architecture please visit:
- The official Pytorch implementation of the architecture: https://github.com/KindXiaoming/pykan
- The research paper: https://arxiv.org/abs/2404.19756

## Experimentation

The implementation of Kolmogorov-Arnold Q-Network (KAQN) offers a promising avenue in reinforcement learning. In this project, we replace the Multi-Layer Perceptron (MLP) component of Deep Q-Networks (DQN) with the Kolmogorov-Arnold Network (KAN). Furthermore, we employ the Double Deep Q-Network (DDQN) update rule to enhance stability and learning efficiency. Initial experiments conducted with KAQN demonstrate its potential in RL tasks. However, challenges persist in effectively applying KAQN to solve the CartPole environment. One such challenge revolves around determining the optimal hyperparameters for this specific setting.

The following plot compare `DDQN` implementation with `KAN` and the classical `MLP` on the CartPole-v1 environment for 500 episodes (with 50 warm-ups episodes).

<center>
<img style="background-color: white" alt="Epsisode length evolution during training on CartPole-v1" src="https://raw.githubusercontent.com/riiswa/kanrl/main/first_result_one_seed.png">
</center>

### TODO

- Find better hyperparameters for KAN to enhance performance and convergence speed.
- Run experiments on multiple seeds to assess the robustness and stability of KAN across different initializations.
- Explore other environments beyond CartPole to evaluate the generalizability and applicability of KAN in diverse RL tasks.


## Installation

The implementation is minimal (< 200 lines of codes), is only require `gymnasium`, `torch`, `numpy` and `pykan`, that can be installed via `pip install -r requirements.txt`.

## Contributing

I welcome the community to enhance this project. There are plenty of opportunities to contribute, like hyperparameters search, benchmark with classic DQN, implementation of others algorithm (REINFORCE, A2C, etc...) and additional environment support.
Feel free to submit pull requests with your contributions or open issues to discuss ideas and improvements. Together, we can explore the full potential of KAN and advance the field of reinforcement learning ❤️.

