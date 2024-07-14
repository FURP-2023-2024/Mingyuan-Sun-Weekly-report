## Weekly Report 4

---
### 1. Test Turtlebot3 with Cartographer Method

**Guidance link:** https://blog.csdn.net/gezongbo/article/details/123388655

### Below are four files in catkin_turtlebot3/src/turtlebot3/turtlebot3_navigation/param

## 1. base_local_planner_params.yaml

 **max_vel_x:** 
  - Maximum linear velocity in the x-direction, set to 0.18 m/s.
- **min_vel_x:** 
  - Minimum linear velocity in the x-direction, set to 0.08 m/s.
- **max_vel_theta:** 
  - Maximum angular velocity, set to 1.0 rad/s.
- **min_vel_theta:** 
  - Minimum angular velocity, set to -1.0 rad/s.
- **min_in_place_vel_theta:** 
  - Minimum in-place rotational velocity, set to 1.0 rad/s.
- **acc_lim_x:** 
  - Maximum acceleration in the x-direction, set to 1.0 m/s².
- **acc_lim_y:** 
  - Maximum acceleration in the y-direction, set to 0.0 m/s². **Change to 1.0 m/s².**(omni project)
- **acc_lim_theta:** 
  - Maximum angular acceleration, set to 0.6 rad/s².
- **xy_goal_tolerance:** 
  - Tolerance for the goal position in meters, set to 0.10 meters.
- **yaw_goal_tolerance:** 
  - Tolerance for the goal orientation in radians, set to 0.05 radians.
- **holonomic_robot:** 
  - Indicates if the robot is holonomic (can move in any direction), set to false. **Change to true.**(omni project)
- **sim_time:** 
  - The amount of time to simulate forward in seconds, set to 0.8 seconds.
- **vx_samples:** 
  - The number of samples to consider for the velocity in the x-direction, set to 18.
- **vtheta_samples:** 
  - The number of samples to consider for the angular velocity, set to 20.
- **sim_granularity:** 
  - The granularity of the simulation in meters, set to 0.05 meters.


## 2. costmap_common_params_burger.yaml

**obstacle_range:** 
  - The maximum distance from the robot at which obstacles are taken into account, set to 3.0 meters.
- **raytrace_range:** 
  - The maximum distance up to which the raytrace is performed for clearing obstacles, set to 3.5 meters.
- **footprint:** 
  - A list of coordinates defining the polygonal footprint of the robot. In this case, it's a square shape.
- **inflation_radius:** 
  - The radius in meters to inflate around obstacles to account for the robot's size and safety margin, set to 1.0 meter.
- **cost_scaling_factor:** 
  - A factor that affects the inflation cost of obstacles, set to 3.0.
- **map_type:** 
  - The type of map being used. Here, it is set to `costmap`.
- **observation_sources:** 
  - The sensors used for observations. Here, it’s just `scan`.
- **scan:** 
  - Specifies the sensor frame (`base_scan`), data type (`LaserScan`), topic (`scan`), and marking and clearing properties (both `true`).

## 3. dwa_local_planner_params_burger.yaml

 **max_vel_x:** 
  - Maximum linear velocity in the x-direction, set to 0.22 m/s.
- **min_vel_x:** 
  - Minimum linear velocity in the x-direction, set to -0.22 m/s.
- **max_vel_y:** 
  - Maximum linear velocity in the y-direction, set to 0.0 m/s.
- **min_vel_y:** 
  - Minimum linear velocity in the y-direction, set to 0.0 m/s.
- **max_vel_trans:** 
  - Maximum translational velocity, set to 0.22 m/s.
- **min_vel_trans:** 
  - Minimum translational velocity, set to 0.11 m/s.
- **max_vel_theta:** 
  - Maximum angular velocity, set to 2.75 rad/s.
- **min_vel_theta:** 
  - Minimum angular velocity, set to 1.37 rad/s.
- **acc_lim_x:** 
  - Maximum acceleration in the x-direction, set to 2.5 m/s².
- **acc_lim_y:** 
  - Maximum acceleration in the y-direction, set to 0.0 m/s².
- **acc_lim_theta:** 
  - Maximum angular acceleration, set to 3.2 rad/s².
- **xy_goal_tolerance:** 
  - Tolerance for the goal position in meters, set to 0.05 meters.
- **yaw_goal_tolerance:** 
  - Tolerance for the goal orientation in radians, set to 0.17 radians.
- **latch_xy_goal_tolerance:** 
  - A boolean to keep the xy goal tolerance once reached, set to false.
- **sim_time:** 
  - The amount of time to simulate forward in seconds, set to 1.5 seconds.
- **vx_samples:** 
  - The number of samples to consider for the velocity in the x-direction, set to 20.
- **vy_samples:** 
  - The number of samples to consider for the velocity in the y-direction, set to 0.
- **vth_samples:** 
  - The number of samples to consider for the angular velocity, set to 40.
- **controller_frequency:** 
  - The frequency at which the controller runs, set to 10.0 Hz.
- **path_distance_bias:** 
  - The weight for the distance to the path in the cost function, set to 32.0.
- **goal_distance_bias:** 
  - The weight for the distance to the goal in the cost function, set to 20.0.
- **occdist_scale:** 
  - The weight for the obstacle cost, set to 0.02.
- **forward_point_distance:** 
  - The distance in front of the robot for scoring trajectories, set to 0.325 meters.
- **stop_time_buffer:** 
  - The amount of time to consider as a buffer for stopping, set to 0.2 seconds.
- **scaling_speed:** 
  - The speed at which to start scaling, set to 0.25 m/s.
- **max_scaling_factor:** 
  - The maximum scaling factor, set to 0.2.
- **oscillation_reset_dist:** 
  - The distance to reset oscillation flags, set to 0.05 meters.
- **publish_traj_pc:** 
  - A boolean to publish the trajectory point cloud, set to true.
- **publish_cost_grid_pc:** 
  - A boolean to publish the cost grid point cloud, set to true.
  - 
## 4. global_costmap_params.yaml

- **global_frame:** 
  - Specifies the coordinate frame used for the global costmap. In this case, it's set to `map`.
- **robot_base_frame:** 
  - Defines the coordinate frame attached to the robot. Here, it is `base_footprint`.
- **update_frequency:** 
  - How often the costmap is updated, in Hz. Set to 10.0 Hz.
- **publish_frequency:** 
  - How often the costmap is published over the ROS topic, in Hz. Set to 10.0 Hz.
- **transform_tolerance:** 
  - The delay tolerated in transform (tf) data, set to 0.5 seconds.
- **static_map:** 
  - A boolean that specifies whether to use a static map (i.e., a pre-built map), set to true.
