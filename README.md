# Learning-to-Discretize-Solving-1D-Scalar-Conservation-Laws-via-Deep-Reinforcement-Learning
source code for Learning to Discretize: Solving 1D Scalar Conservation Laws via Deep Reinforcement Learning

We will add a lot more comments, and code clean later.
For a breif reference usage at the moment:

train commands
python main_burgers.py --flux u2 --mode weno_coef_four --num_process xxx --agent ddpg (should set num_process >= init_util.py line 175 len(train_idxes)). (do not set num_process to be too large, or the replay buffer size would be too large and causes MemError. 4 is ok.)

for test trained models, and plot the evolving animations
python main_burgers.py --flux u3 --test True --animation 1 --load_path xxx --save_RL_weno_animation xxx --Tscheme euler/rk4
