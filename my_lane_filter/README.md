# Package `lane_filter` {#lane_filter}

Assigned: Liam

<move-here src='#lane_filter-autogenerated'/>


## `lane_filter_node` {#lane_filter-lane_filter_node}

<move-here src="#lane_filter-lane_filter_node-autogenerated"/>

This package runs the lane filtering during lane control mode. There are two functionalities implemented. The first one is the estimation of the actual position. This position consist of a distance $d$ form the center of the line and an angle $phi$ with respect to the center of the lane. 

Additionally there is a basic curvature estimation implemented. This functionality is able to predict if there is a straight line or one of the standard left or right curves of Duckietown ahead of the robot. The curvature estimation is not yet very robust. The variable curvature_res is by default set to 0, which means the curvature estimation is switched off. The get a more or less fine estimation curvature_res needs to be around 4, which also adds a delay to the system that again lowers the performance of the Duckiebot.

To run the code the lane following demo can be used.

    $ make demo-lane-following 
