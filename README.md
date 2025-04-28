# GELLO

## Single XArm teleop control in sim - commands to run the teleoperation
First test your GELLO with a simulated robot to make sure that the joint angles match as expected.
In one terminal run
```
python experiments/launch_nodes.py --robot <sim_ur, sim_panda, or sim_xarm>
```
This launched the robot node. A simulated robot using the mujoco viewer should appear.

Then, launch your GELLO (the controller node).
```
python experiments/run_env.py --agent=gello
```
You should be able to use GELLO to control the simulated robot!

## Bimanual teleop in sim -  commands to run the teleoperation
1. Go to the gello_software directory on 2 terminals.
2. run the command
   ```
   python3 experiments/launch_nodes.py --robot sim_xarm_bimanual
   ```
   in one of the terminals.
3. On the other terminal run the command -
   ```
   python3 experiments/run_env.py --agent=gello --bimanual
   ```
4. You will see a mujoco terminal with 2 XArms spawned . You will also be able to control both the XArms using the teleoperation structures, provided they are calibrated correctly.


# Citation

```
@misc{wu2023gello,
    title={GELLO: A General, Low-Cost, and Intuitive Teleoperation Framework for Robot Manipulators},
    author={Philipp Wu and Yide Shentu and Zhongke Yi and Xingyu Lin and Pieter Abbeel},
    year={2023},
}
```

# License & Acknowledgements
This source code is licensed under the MIT license found in the LICENSE file. in the root directory of this source tree.

This project builds on top of or utilizes the following third party dependencies.
 * [google-deepmind/mujoco_menagerie](https://github.com/google-deepmind/mujoco_menagerie): Prebuilt robot models for mujoco
 * [brentyi/tyro](https://github.com/brentyi/tyro): Argument parsing and configuration
 * [ZMQ](https://zeromq.org/): Enables easy create of node like processes in python.
