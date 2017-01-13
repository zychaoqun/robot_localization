robot_localization
==================

robot_localization is a package of nonlinear state estimation nodes. The package was developed by Charles River Analytics, Inc.

Please see documentation here: http://wiki.ros.org/robot_localization
-----------------------------------------------------------------------------------------------------------------------------
Debug log

Run which node:

simply run the ekf_template.launch

edit ekf_template.launch :
for example, you just have one odom, and the topic is /odom, then:
edit the ekf_template.yaml
---------------------------------------------
from:  odom0: example/odom to  odom0: odom   
from:  
map_frame: map              # Defaults to "map" if unspecified  
odom_frame: odom            # Defaults to "odom" if unspecified  
base_link_frame: base_link  # Defaults to "base_link" if unspecified  
world_frame: odom   
to:  
map_frame: map              # Defaults to "map" if unspecified  
odom_frame: odom            # Defaults to "odom" if unspecified  
base_link_frame: base_footprint  # Defaults to "base_link" if unspecified,here base_link has already published and its parent frame is base_footprint, so here we set bsed_link_frame as base_footprint  
world_frame: map  # you can get tf of map-> odom if you set this  

