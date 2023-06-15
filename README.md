# Super-Mario-Bros-PPO-Stable-baselines
Creating a PPO agent to solve the first level of Super Mario Bros using stable baselines 3

## Introduction
I'm a master student in Computer science and history in the faculty of arts at Lausanne University. For one of my project I decided to try and complete the first level of Super Mario Bros using the PPO implementation from [Stable Baselines 3 library](https://stable-baselines3.readthedocs.io/en/master/modules/ppo.html). This was not an easy task as I only had one course in machine learning and had to learn reinforcement learning from scratch. I spent a lot of time watching videos, following tutorials and then I followed the [hugging face course on reinforcement learning](https://huggingface.co/learn/deep-rl-course/unit0/introduction?fw=pt) to get a basic understanding of what I was getting myself into.

After the course, I mainly tried to replicate a succesful implementation from [Viet Nguyen](https://github.com/uvipen/Super-mario-bros-PPO-pytorch/), but was unable to, because his implementation of the PPO algorithm is slightly different than the one from stable baselines. Inded, after tweaking the parameters of the stable baselines  ppo implementation as well as the learning rate I realized it had been a waste of time and the results supported that conclusion. Then I came across a youtube video from [ClarityCoders](https://www.youtube.com/watch?v=PxoG0A2QoFs). In this video I realized he changed almost none of the parameters and managed to finished the first level and achieved an average rewards around 3000. 

One of the most important things he did was in the preprocessing of the environement, he set a maxstep per episode of 20000. According to his experience in solving games with RL, he noticed it has a high impact on the agent's performance. After trying to replicate his implementation, I manageed to reach an average reward of 18000 wich was higher than all my previous attempts and was better than another Master thesis work I also inspired myself from[^1]. My PPO agent is not yet able to compllete the first level consistently, but only 17.4 percent of the time. I suppose it's due to the fact that I couldn't replicate the exact number of paralel environements used by Clarity Coders. My kernel would crash every time I tried to use more than two parallel enviornments. I suppose this is du to the fact that I have not access to GPUs wich are powerful enough : 16gb only, when at least 32gb would have been necessary. 

Despite my first experience with reinforcement learning feeling like a pay-to-win, I learned a lot on how to approach a complex problem from scratch and gain a lot of confidence in my coding abilities. I also take with a lot of joy the small win of being able to do a slightly better model than the one from a Master thesis on the subject[^1].

## How to use my code
Just make sure to download the requirements.txt file, then you can simply execute code in the jupyter notebook. I used this code in [Gradient Notebooks](https://www.paperspace.com/gradient/notebooks), so if you have problems of compatibilty runnning it on your machine or in Google Colab, just make a free account there, upload the notebook, the requirements.txt file and the models, and you should be all set.
Open the notebook and there you can train a model, train a previously trained model, create videos of the model in the environement and also get statistics from how well your model performs. Before doing anything you should run the first and second cells of code : the pip install and the imports without forgetting to restart your kernel in between. Read carefully the instructions I gave you in the notebook and everything should be fine.

## Results

Based on a 1000 consecutive episode the success rate of my agent is 17.4 percent in the "SuperMarioBros-1-1-v0" environement (1 life only). His mean reward is at 1860, wich is lower than the approximate 3000 required to finish the level. If you want to train a succesful agent and you have a powerful GPU you can take the same parameters I have and change the number of environements from two to four. I would be very interested to see people manage to create an agent that gets an average reward of 3000. Don't hesitate to contact me if you have any questions.

## Bonus Video of my agent finishing the level


https://github.com/Joel7815/Super-Mario-Bros-PPO-Stable-baselines/assets/101325473/04dde224-7303-405c-bb5d-efd5784337ef





[^1]: ZONE, Corentin. Deep Reinforcement Learning: An introduction through video games. Faculté des sciences, Université catholique de Louvain, 2022. Prom. : Van Oirbeek, Robin ; Pennisi, Andrea. (Thèse de master). Disponible en ligne : https://dial.uclouvain.be/memoire/ucl/object/thesis:38002. Consulté le 18.03.2023
