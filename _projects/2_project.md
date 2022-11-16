---
layout: page
title: Perception and Obstacle Avoidance
description: A real-time dynamic obstacle tracking and mapping system for UAV navigation and collision avoidance
img: assets/img/vision.jpg
importance: 2
category: work
---

While plenty of sophisticated learning-based dynamic obstacle detection algorithms exist in autonomous driving, the quadcopter’s limited computation resources cannot achieve real-time performance using those approaches. We propose a real-time dynamic obstacle tracking and mapping system for quadcopter obstacle avoidance using an RGB-D camera. The main contributions are as follow:

• <strong>Region proposal detector with map refinement:</strong> We apply a lightweight depth image detector to obtain obstacle region proposals and uses the static map to refine the obstacles’ bounding boxes.

• <strong>Dynamic obstacle identification and tracking:</strong> We
apply the Kalman filter and our continuity filter to track and identify dynamic obstacles. The dynamic-region cleaning approach is then applied to clean the remained trails of dynamic obstacles in the static map.

• <strong>Environment-aware trajectory prediction:</strong> The proposed Markov chain-based dynamic obstacle trajectory prediction method considers the interaction between dynamic obstacles and the static environment based on
the trajectory probability distribution.

See the related [Paper] (https://arxiv.org/pdf/2209.08258.pdf) if you are interested.

<div align="center">
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Dynamic_Modules.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
The system contains three dynamic modules
with one static occupancy map module. It takes the depth images with the
robot poses as the inputs and outputs cleaned static maps and dynamic
obstacle states with their predicted trajectories.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/EKF.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Visual.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Left is the illustration of the trajectory prediction. At the time t − 1, all five paths in the path library are safe, so path 3 has the highest probability. However, at time t, the previously safe paths 2,3 in the path library are not safe anymore. So, the final prediction is path 4. Right, visualization of obstacle tracking results in simulation.
</div>
</div>

The simulation and physical experiments show that our methods can successfully track and represent obstacles in dynamic environments in real-time and safely avoid obstacles.

<div align="center">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Elql8FrDtUk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
