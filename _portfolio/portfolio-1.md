---
title: "Project 1"
excerpt: "Short description of portfolio item number 1<br/><img src='/images/500x300.png'>"
collection: portfolio
---

Topics: Real-Time Balancing of a Quadrupedal Robot through Optimization of Cartesian Centre-of-Mass Impedances using Reinforcement Learning

# Summary:
This project make use of whole body control scheme combing with DCM indicator and impedance control scheme. It employs reinforcement learning to enhance the selection of gain parameters, ultimately achieving superior performance when compared to traditional and binary impedance control methods. Additionally, it can adaptively select the optimal gain settings based on varying disturbance profiles.

# Project Description

# ❓Main Problem:
Controlling a quadruped robot presents a significant challenge in legged robot applications due to its higher number of Degrees of Freedom (DoFs) and the coupling effects between its connectors that cannot be ignored. Moreover, it is essential for the robot to exhibit compliance and effectively interact with its environment. Therefore, the proposed control scheme is as follows.

![Control Structure](control structure (1).png)

However, classical binary gains used in impedance control strategies tend to make the robot overly stiff and incapable of adapting to diverse environments and various disturbances. This occurs because in an impedance control strategy, the damping and stiffness gains have a direct impact on the external forces applied in the robot's feet. This, in turn, affects the robot's overall stability. When external disturbances occur, the system should tend to opt for smaller gain values to minimize the external forces acting on the robot's feet, allowing the robot to maintain contact with the ground for an extended duration. Once stability is restored, it becomes necessary to increase these gains to enhance the precision of task execution. This process cannot be efficiently managed using fixed binary gain settings because the robot cannot be continuously supervised. Consequently, an automated gain adjustment mechanism is necessary.

To address this challenge, reinforcement learning is employed. Therefore, this project leverages deep reinforcement learning (DRL), specifically TD3 (Twin Delayed Deep Deterministic Policy Gradients), to tackle this problem.


# Result :
After training, the final result could be shown in the following.

When comparing the performance of reinforcement learning (RL) with binary gains, it becomes evident that RL outperforms in both anti-disturbance capability and tracking capability. The red line represents the results achieved using RL, while the lines of other colors correspond to those obtained with binary gains.
![Comparison with different binary in X dimension](images/gain_comparison_x (1).png)
![Comparison with different binary in Y dimension](images/gain_comparison_y (1).png)
![Comparison with different binary in Z dimension](images/gain_comparison_z (1).png)


# Demos:
There are two scenarios:
Firstly, when applying a 5N force to the robot's base at regular time intervals, it is evident that RL promptly detects and responds to this disturbance by making immediate gain adjustments.

Secondly, during random dragging tests where the robot experiences unpredictable and varying disturbances, the robot exhibits the capability to recover swiftly and respond effectively. This adaptability underscores the effectiveness of the RL-based control approach.
 
<video width="320" height="240" controls>
    <source src="introduction.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>







