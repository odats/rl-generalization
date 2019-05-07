# rl-generalization

____________________________________________________________
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
