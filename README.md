[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42135622-e55fb586-7d12-11e8-8a54-3c31da15a90a.gif "Soccer"


# Project 3: Collaboration and Competition

### Introduction

For this project, I will work with the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment.

![Trained Agent][image1]

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1.  If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.  Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.  Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. 

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single **score** for each episode.

The environment is considered solved, when the average (over 100 episodes) of those **scores** is at least +0.5.

### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)

2. Place the file in the DRLND GitHub repository, in the `p3_collab-compet/` folder, and unzip (or decompress) the file. 

### Instructions

1. Follow the instructions in `Tennis.ipynb` to get started with training your own agent!  

2. Make sure you got python 3 and anacoda installed. To install anacoda, please refer to this link [Anacoda](https://www.anaconda.com/download/)

3. Setup anacoda deep reinforcement learning environment by create (and activate) a new environment with Python 3.6.
* **Linux** or **Mac**:
```
conda create --name drlnd python=3.6
source activate drlnd
```

* **Windows:**
```
conda create --name drlnd python=3.6 
activate drlnd
```

4. Clone the repository and install the requirements
```
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```
5. Create and IPython Kernel for the drlnd environment and select the environment in jupyter notebook
```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

6. (optional) get requirement.txt by using 
```
$pip freeze > requirements.txt.
```

### Instructions

Follow the instructions in `Tennis.ipynb` to get started with training your own agent!  


(_For AWS_) If you'd like to train the agent on AWS, you must follow the instructions to [set up X Server](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above.

1. Request service limit increase in AWS for p2.xlarge instance

2. Launch an p2.xlarge instance using Deep Learning AMI with Source Code (CUDA8,Uubntu) AMI

3. Create a new security group set Protocol to TCP, port range as 8888 and SSH to the instance

4. In order to create a config file for jupyter notebook settings.
```
jupyter notebook --generate-config
```

5. Clone the repo for this projec then install the requirements
```
sudo python3 -m pip install -r requirements/requirements-gpu.txt
```

6. Start the notebook
```
jupyter notebook --ip=0.0.0.0 --no-browser
```

7. Access the notebook from local browser. Access the Jupyter notebook index from your web browser by visiting: X.X.X.X:8888/?token=... (where X.X.X.X is the IP address of your EC2 instance and everything starting with :8888/?token= is what you just copied).

### Run the code

Open Tennis.ipynb in Jupyter and press Ctrl + Enter to run the code cell from first line to the last (Instruction is written in code cell)