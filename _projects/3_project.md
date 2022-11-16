---
layout: page
title: Power System 
description: Voltage Control based on ISS Neural Certificates
img: assets/img/power_flow.png
# redirect: https://unsplash.com
importance: 3
category: work
---

We Developed methods for stabilizing large scale power systems based on Input-to-State Stability (ISS) Lyapunov-based neural certificate, by treating a large system as an interconnection of smaller subsystems. Each ISS
Lyapunov function of subsystem could be collected to prove the global stability of power system.

For smart-grid simulation, we utilized Pandapower tool for modelling and of multiple power system cases. The Neural controllers and Lyapunov functions show great performance in voltage convergence and stability of power systems.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/eval_voltatges_4bus.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/ref_voltages_4bus.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>

</div>
<div class="caption">
    Left is the performance of Neural Controller. Right, we take a simple P-controller for reference.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/eval_voltatges_4bus.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/lyapunov_values.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>

</div>
<div class="caption">
    Left, descent violation figure. Right, Heatmap of Lyapunov value.
</div>
Future Plan: Scale up to larger Power System (TO BE UPDATED)