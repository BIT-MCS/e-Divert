# e-Divert
This is the code accompanying the paper: "[Distributed and Energy-Efficient Mobile Crowdsensing with Charging Stations by Deep Reinforcement Learning](https://ieeexplore.ieee.org/abstract/document/8821415)", published in TMC.

## :page_facing_up: Description
Mobile crowdsensing (MCS) represents a new sensing paradigm that utilizes the smart mobile devices to collect and share data. Traditional MCS systems mainly leverages the people carried smartphones and other wearable devices which are constrained by the limited sensing capability and battery power. With the popularity of unmanned vehicles like unmanned aerial vehicles (UAVs) and driverless cars, they can provide much more reliable, accurate and cost-efficient sensing services due to to their equipped more powerful sensors. In this paper, we propose a distributed control framework for energy-efficient and DIstributed VEhicle navigation with chaRging sTations, called “e-Divert”. It is a distributed multi-agent deep reinforcement learning (DRL) solution, which uses a convolutional neural network (CNN) to extract useful spatial features as the input to the actor-critic network to produce a real-time action. Also, e-Divert incorporates a distributed prioritized experience replay for better exploration and exploitation, and a long short-term memory (LSTM) enabled N-step temporal sequence modeling module. The solution fully explores the spatiotemporal nature of the considered scenario for better vehicle cooperation and competition between themselves and charging stations, to maximize the energy efficiency, data collection ratio, geographic fairness, and minimize the energy consumption simultaneously.

## :wrench: Installation
1. Clone repo
    ```bash
    git clone https://github.com/BIT-MCS/e-Divert.git
    cd e-Divert
    ```
2. Install dependent packages
    ```sh
    conda create -n mcs python==3.8
    conda activate mcs
    pip install tensorflow-gpu==1.15
    pip install -r requirements.txt
    ```


## :computer: Training

Train our solution
```bash
python experiments/train.py --num_actor_workers=5 
```
## :checkered_flag: Testing

Test with the trained models 

```sh
python experiments/test.py --load-dir=your_model_path
```

Random test the env

```sh
python experiments/test_random.py
```

## :clap: Reference
- https://github.com/openai/maddpg


## :scroll: Acknowledgement

This paper was financially supported by National Natural
Science Foundation of China (No. 61772072).
<br>
Corresponding author: Chi Harold Liu.

## :e-mail: Contact

If you have any question, please email `3120215520@bit.edu.cn`.

## Paper
If you are interested in our work, please cite our paper as

```
@ARTICLE{liu2021distributed,
    author={Liu, Chi Harold and Dai, Zipeng and Zhao, Yinuo and Crowcroft, Jon and Wu, Dapeng and Leung, Kin K.},
    journal={IEEE Transactions on Mobile Computing},
    title={Distributed and Energy-Efficient Mobile Crowdsensing with Charging Stations by Deep Reinforcement Learning},
    year={2021},
    volume={20},
    number={1},
    pages={130-146},
}
```
