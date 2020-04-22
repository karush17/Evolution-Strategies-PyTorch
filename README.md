 ![Hex.pm](https://img.shields.io/hexpm/l/plug?style=plastic)  
 
<img src="gifs\BipedalWalker.gif" align="center" height="200" width="200" /><img src="gifs\LunarLander.gif" align="center" height="200" width="200" /><img src="gifs\Hopper.gif" align="center" height="200" width="200" /><img src="gifs\Swimmer.gif" align="center" height="200" width="200" />  

<img src="gifs\HalfCheetah.gif" align="center" height="200" width="200" /><img src="gifs\InvertedPendulum.gif" align="center" height="200" width="200" /><img src="gifs\Reacher.gif" align="center" height="200" width="200" /><img src="gifs\Humanoid.gif" align="center" height="200" width="200" />  
<img src="gifs\Thrower.gif" align="center" height="200" width="200" /><img src="gifs\HumanoidStandup.gif" align="center" height="200" width="200" />


# Introduction
Evolution Strategies (ES) have proven to be an effective technique for training continuous as well as discrete control tasks. By making use of Gaussian perterubations in the weight space, ES eliminate the need for backpropagation and reduce the computation time by a significant extent when making use of parallelization. This has allowed scalability in the Reinforcement Learning paradigm.  

This tutorial is a naive implementation of ES proposed in OpenAI's [blog post](https://openai.com/blog/evolution-strategies/) and [paper](https://arxiv.org/pdf/1703.03864.pdf). A detailed implementation of OpenAI's version can be found at their [Github repository](https://github.com/openai/evolution-strategies-starter).  

<h3>NOTE-</h3> All implementations of ES (including this tutorial) require effective computational and parallelization resources such as multiple CPU cores. Experiments for this tutorial were conducted on a virtual AWS EC2 instance consisting of 96 CPU cores and 384 GB of memory. 

# Dependencies
```  
ubuntu 18.04  
python 3.6  
numpy 1.18.0  
torch 1.4.0  
gym 0.15.4  
box2d 2.3.8  
mujoco 1.50.1.59  
```  

# Usage
Download the repository, extract the contents and simply run the ipynb in Jupyter Notebook.  
```  
jupyter notebook Evolution_Strategies.ipynb
```  

Run in Python using the following-  
```  
ipython nbconvert --to script Evolution_Strategies.ipynb  
python3 Evolution_Strategies.py
```  

# Tips
* MuJoCo is a difficult package to setup as it varies for each platform. Make sure to build it from source and specific to your system. A tutorial for the same can be found [here](https://github.com/reinforcement-learning-kr/pg_travel/wiki/Installing-Mujoco-py-on-Linux).  
* The parameter MAX_WORKERS should be handled carefully since training on multiple CPUs requires more processes and can often lead to poor performance.  
* SIGMA is a tricky hyperparameter to tune. Often at times it will yield good evolutions in weight spaces but for some environments it may not lead to full convergence.  

# Results
<img src="results\results-1.PNG" align="center" height="1000" width="900" />  
<img src="results\results-2.PNG" align="center" height="1000" width="900" />  
<img src="results\results-3.PNG" align="center" height="250" width="900" />  



