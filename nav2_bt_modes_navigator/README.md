# BT Modes Navigator

The BT Modes Navigator (Behavior Tree System Modes Navigator) module implements the [NavigateToPose task interface](../nav2_behavior_tree/include/nav2_behavior_tree/navigate_to_pose_action.hpp) using [ROS2 System Modes](https://github.com/microROS/system_modes).

# Launching bt_modes_navigator demo.

  Launch gazebo sim and nav2 system (gazebo headless mode ON) -- ```ros2 launch nav2_bringup nav2_tb3_system_modes_sim_launch.py```
  
  Run ```ros2 run system_modes mode-manager [path]/nav2_modes.yaml```(nav2_modes example in nav2_bt_modes_navigator/system_modes/nav2_modes.yaml) to able the change of nav2 modes.
  
 Finally call the service to change the mode -- ```ros2 service call [/node]/change_mode system_modes/ChangeMode "{node_name: 'node_name', mode_name: 'MODE_NAME'}"``` -- (example ```ros2 service call /bt_navigator/change_mode system_modes/ChangeMode "{node_name: 'navigation2', mode_name: 'BATTERY_CONTINGENCY'}" ```)
 
 
  
  
