# Agent adaptation to a changing environment

Machine Learning Project

## GitHub repository structure

`Project Final Report` - final project report

`models` - folder with trained agents on AWS instance in Pong environment

`DQN_for_Sunblaze_CartPole_(DRE),_openai_baseline` - ipython notebook file with agent in CartPole environment

`Pong_game_play` - ipython notebook file with agent in Pong environment (uses trained agents)

`Q-learning FrozenLake` - ipython notebook file with agent in FrozenLake environment

`Project Progress Report` - midterm project report

## Prerequisites and References

pip install --upgrade pip
python3 -m venv openai_env
source openai_env/bin/activate
git clone https://github.com/openai/baselines.git
pip install tensorflow
cd baselines
pip install -e .
pip install gym[atari] 

python -m pip install jupyter

____________________________________________________________
monitoring
watch -n 1 nvidia-smi
sudo apt-get install htop

____________________________________________________________
update baselines
decrease learning rate
checkpoint_path="pong_checkpoint",
print_freq=10,

edit
https://github.com/openai/baselines/blob/master/baselines/deepq/deepq.py

from baselines.common.atari_wrappers import make_atari

from baselines.common.atari_wrappers import LazyFrames

new_obs = add_noise_frames(new_obs, 0.005, 0.005)

____________________________________________________________
https://github.com/sunblaze-ucb/rl-generalization
https://openai.com/blog/openai-baselines-dqn/
https://github.com/openai/baselines
https://github.com/openai/baselines/tree/master/baselines/deepq/experiments
https://github.com/tensorpack/tensorpack/tree/master/examples/DeepQNetwork
https://medium.com/mlreview/speeding-up-dqn-on-pytorch-solving-pong-in-30-minutes-81a1bd2dff55
https://github.com/google/dopamine/blob/master/dopamine/colab/cartpole.ipynb
https://github.com/sunblaze-ucb/rl-generalization

30min Pong
https://github.com/PacktPublishing/Deep-Reinforcement-Learning-Hands-On/blob/master/Chapter06/02_dqn_pong.py#L153
https://github.com/PacktPublishing/Deep-Reinforcement-Learning-Hands-On/blob/master/Chapter06/03_dqn_play.py	

