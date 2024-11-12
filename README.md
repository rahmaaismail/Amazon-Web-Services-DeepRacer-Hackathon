# Amazon-Web-Services-DeepRacer-Hackathon
AWS DeepRacer is a cloud-based autonomous racing platform designed by Amazon to help people learn and experiment with reinforcement learning (RL) in a fun and engaging way. With AWS DeepRacer, users can train and evaluate machine learning models for autonomous driving using small, 1/18th-scale race cars in a simulated environment, and then optionally deploy those models onto physical DeepRacer cars for real-world testing.

Here’s a quick rundown of the main components and features:

Reinforcement Learning (RL) Models: DeepRacer is built to teach RL, where the model learns to drive by receiving rewards for good actions and penalties for bad ones. The goal is to optimize a driving policy that helps the car complete a track quickly and safely.

AWS DeepRacer Console: This is the online interface where users can train models, choose track configurations, define reward functions, and view simulations. It’s an accessible way to start with RL even if you don’t have prior machine learning experience.

Physical DeepRacer Car: The physical version is equipped with sensors and a camera and can run trained models from the AWS DeepRacer Console. It’s a great tool for testing your models in a real-world environment.

Racing League and Community: AWS DeepRacer League is a global racing competition where participants submit their models to compete on different tracks. There are virtual races, and at select events, live physical races. It’s a way to learn, collaborate, and improve RL skills.

This project focuses on training an AWS DeepRacer model to navigate the re:Invent 2018 track using reinforcement learning. The model is designed to optimize speed, stability, and control, leveraging a custom reward function to achieve competitive lap times on the challenging track layout.

Project Overview
AWS DeepRacer provides a fun and practical way to experiment with reinforcement learning (RL). This project uses RL principles to create a model that can autonomously drive a 1/18th-scale race car around the re:Invent 2018 track, optimizing for factors like lane positioning, speed, and turn handling.

The re:Invent 2018 track has a series of straight sections and turns that require strategic control of speed and positioning. The reward function created here helps guide the DeepRacer car through the track efficiently, minimizing off-track penalties and maximizing progress.

Reward Function
The reward function is the core of this model's training strategy. This function rewards the car for staying close to the track center, controlling speed based on steering angle, and completing the track quickly. Here’s an outline of the key elements:

Reward Function Logic
Centerline Reward: Rewards the car for staying close to the center of the track. This reduces the risk of going off-track, especially in turns.

Speed and Steering Control: The function rewards the car for maintaining a higher speed on straight sections but moderates speed in sharp turns by factoring in the steering angle. This encourages controlled driving on turns while maximizing speed on straights.

Progressive Reward: Adds a bonus based on the car’s progress through the track, motivating the car to complete laps efficiently.

Straight-Line Bonus: Rewards minimal steering angle on straight sections, promoting smooth, stable driving on track sections that do not require turning.
