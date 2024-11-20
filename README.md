# Amazon-Web-Services-DeepRacer-Hackathon
AWS DeepRacer is a cloud-based autonomous racing platform designed by Amazon to help people learn and experiment with reinforcement learning (RL) in a fun and engaging way. With AWS DeepRacer, users can train and evaluate machine learning models for autonomous driving using small, 1/18th-scale race cars in a simulated environment, and then optionally deploy those models onto physical DeepRacer cars for real-world testing.

Here’s a quick rundown of the main components and features:

Reinforcement Learning (RL) Models: DeepRacer is built to teach RL, where the model learns to drive by receiving rewards for good actions and penalties for bad ones. The goal is to optimize a driving policy that helps the car complete a track quickly and safely.

AWS DeepRacer Console: This is the online interface where users can train models, choose track configurations, define reward functions, and view simulations. It’s an accessible way to start with RL even if you don’t have prior machine learning experience.

Physical DeepRacer Car: The physical version is equipped with sensors and a camera and can run trained models from the AWS DeepRacer Console. It’s a great tool for testing your models in a real-world environment.

Racing League and Community: AWS DeepRacer League is a global racing competition where participants submit their models to compete on different tracks. There are virtual races, and at select events, live physical races. It’s a way to learn, collaborate, and improve RL skills.

This project focuses on training an AWS DeepRacer model to navigate the re:Invent 2018 track using reinforcement learning. The model is designed to optimize speed, stability, and control, leveraging a custom reward function to achieve competitive lap times on the challenging track layout.

# Project Achievements
Out of 31 teams in the initial racing round, our model achieved an outstanding 4th place, showcasing its precision and performance. Advancing to the Top 10 round, we secured a strong 6th place overall, reflecting a balance between speed, stability, and strategic track handling.

The track was the re:Invent 2018 features a mix of straight sections and challenging curves, requiring precise speed control and lane positioning. This project focused on strategic handling to maximize efficiency, using a custom reward function tailored to the track's unique layout.

# Reward Function
The reward function is the core component that drives the model's learning. It assigns rewards or penalties based on various factors, guiding the car to improve its driving policy. Here's a breakdown of the logic:

# Key Features
Centerline Reward:

Encourages the car to stay close to the track center to minimize off-track penalties and improve stability.
Speed and Steering Control:

Rewards higher speeds on straight sections while encouraging slower, controlled driving on sharp turns to prevent zig-zag behavior.
Progressive Reward:

Incentivizes the car to complete laps efficiently by rewarding progress through the track.
Straight-Line Bonus:

Rewards minimal steering angles on straight sections to promote smooth, stable driving.
Curvature Adaptation:

Adjusts rewards based on the track's curvature, guiding the car to optimize its speed and stability based on upcoming turns.
Code Highlights: Reward Function
The custom reward function is implemented in Python and incorporates various considerations to optimize performance. Below is a high-level outline of its logic:

Staying on Track: Rewards for all wheels remaining on the track.
Centerline Distance: Gradual rewards based on proximity to the centerline.
Speed Management:
High speed on straight sections.
Reduced speed on curves to maintain control.
Steering Angle Penalties: Avoids excessive steering to prevent zig-zag behavior.
Curvature Awareness: Adjusts driving behavior dynamically based on track curvature and direction.
