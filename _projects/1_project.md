---
layout: page
title: Vision-aided Path planning
description: Vision aided UAV Navigation and Dynamic Obstacle Avoidance using Gradient based B spline Trajectory 
img: assets/img/planning.jpg
importance: 1
category: work
---
Navigating dynamic environments requires the robot to generate collision-free trajectories and actively avoid moving obstacles. Most previous works designed path planning algorithms based on one single map representation, such as the geometric, occupancy, or ESDF map. Although they have shown success in static environments, due to the limitation of map representation, those methods cannot reliably handle static and dynamic obstacles simultaneously. To address the problem, We proposes a gradient-based B-spline trajectory optimization algorithm utilizing the robot’s onboard vision. The main contributions of this work are:

• <strong>Vision-aided 3D Dynamic Map:</strong> This algorithm utilizes the depth image with the occupancy voxel map to track 3D dynamic obstacles and adopts this 3D dynamic map to perform the trajectory optimization.

• <strong>Circle-based Guide-Point Algorithm</strong>: We propose the guide-point algorithm to approximate the costs and gradients of static collisions for trajectory optimization.

• <strong>Receding Horizon Distance Field</strong>: The proposed receding horizon distance field utilizes the obstacles’ future predictions to estimate the collision costs and gradients for preventing dynamic collisions.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/dynamic_map.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/circle_guide.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/receding_horizon.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

To evaluate the proposed method’s performance, we conduct simulation experiments and physical flight tests in dynamic environments. See the [paper](https://arxiv.org/pdf/2209.07003.pdf) if you are interested.

<div align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Elql8FrDtUk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

