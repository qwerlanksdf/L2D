# Learning-to-Discretize-Solving-1D-Scalar-Conservation-Laws-via-Deep-Reinforcement-Learning
source code for Learning to Discretize: Solving 1D Scalar Conservation Laws via Deep Reinforcement Learning

We will add a lot more comments, and code clean later.
For a breif reference usage at the moment (if you are eager to explore, just read the get_args.py to see how you can set a large number of args)

train commands  
python main_burgers.py --flux u2 --mode weno_coef_four --num_process xxx --agent ddpg (should set num_process >= init_util.py line 175 len(train_idxes)). (do not set num_process to be too large, or the replay buffer size would be too large and causes MemError. 4 is ok.)

for test trained models, and plot the evolving animations  
python main_burgers.py --flux u2 --test True --animation 1 --load_path xxx --save_RL_weno_animation xxx --Tscheme euler/rk4

We've provided a pre-trained model: 6150ddpgactor.txt and 6150ddpgcritic.txt. To make some evolving demos with the trained models, just run:  
python main_burgers.py --flux u2 --test True --animation 1 --load_path ./6150 --agent ddpg --show_RL_weno_animation 1 --Tscheme rk4 --hidden_layer_num 6
