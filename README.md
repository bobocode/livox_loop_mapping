## livox_loop_mapping
This is a repository for Livox LiDARS mapping with loop detection.
**Note:** This is the basic framework for Livox LiDARS mapping with loop detection. It cannot be used for all version of Livox LiDARS. It is suggested that the point cloud is dense enough. And the range image transfered from the point cloud is still in debugging to find better parameters.
Some key issues:
1. Different feature extraction;
2. transfer point cloud to range image, build keyframe database, and detect loop by matching visual features;


In the development of our package, we reference to livox_mapping,image_lidar_place_recognition .
## 1. Prerequisites
### 1.1 **Ubuntu** and **ROS**
Ubuntu 64-bit 16.04 or 18.04.
ROS Kinetic or Melodic. [ROS Installation](http://wiki.ros.org/ROS/Installation)

### 1.2. **PCL && Eigen && openCV**
Follow [PCL Installation](http://www.pointclouds.org/downloads/linux.html).
Follow [Eigen Installation](http://eigen.tuxfamily.org/index.php?title=Main_Page).
Follow [openCV Installation](https://opencv.org/releases/).

### 1.3. **livox_sdk**
Follow [Livox_SDK Installation](https://github.com/Livox-SDK/Livox-SDK).

### 1.4. **livox_ros_driver**
Follow [livox_ros_driver Installation](https://github.com/Livox-SDK/livox_ros_driver).

### 1.5. **DOW3**
Follow [DOW3 Installation](https://github.com/rmsalinas/DBow3).


## 2. Build
Clone the repository and catkin_make:

```
    cd ~/catkin_ws/src
    git clone https://github.com/bobocode/livox_loop_mapping.git
    cd ..
    catkin_make
    source ~/catkin_ws/devel/setup.bash
```
## 3. Test Package
Run the launch file:

```
roslaunch livox_loop_mapping mapping_loop.launch
rosbag play ROSBAGFILE
```
## 5.Acknowledgments
Thanks for livox_mapping, [livox_mapping](https://github.com/Livox-SDK/livox_mapping) and imaging_lidar_place_recognition, [imaging_lidar_place_recognition](https://github.com/TixiaoShan/imaging_lidar_place_recognition).
