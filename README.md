# ros_csv_extraction
CSV Data Extraction Tool for ROS bag files.
ROS (robot operating system) is a software system gaining popularity in robotics for control and automation.

This repository provides a tool to extract data to CSV format for a number of ROS message types for analysis in other software.

See original post on this code at http://www.shanelynn.ie/csv-data-extraction-tool-for-ros-bag-files/

Feel free to augment and enjoy.

# ROS Message Types
Thus far, the data extraction tool is compatible with the following ROS message types:

* sensor_msgs/Image
* sensor_msgs/Imu
* sensor_msgs/LaserScan
* sensor_msgs/NavSatFix
* gps_common/gpsVel
* umrr_driver/radar_msg (this was a type used by the CRUISE vehicle (see http://www.shanelynn.ie/csv-data-extraction-tool-for-ros-bag-files/))
* nav_msgs/Odometry

To install the data extraction tool, clone it to the `src` folder in your catkin_workspace, and `run catkin_make --pkg ros_csv_extraction`before using.

# Usage
 * Extract all compatible topics in a bag file:

`rosrun ros_csv_extraction extract_all -b <path_to_bag_file> -o <path_to_output_dir>`

 * Extract a single topic:

`rosrun ros_csv_extraction extract_topic -b <path_to_bag_file> -o <path_to_output_dir> -t <topic_name>`