[中文文档](https://github.com/RoboSense-Robotics/robosense_ac_studio/blob/main/README_CN.md)

## 1. Introduction

This warehouse mainly stores AC1 super sensor repo multi-warehouse management warehouse files. Through this warehouse, the drivers, algorithms, tools and other warehouses provided by AC_Studio can be fully pulled, which is convenient for warehouse pulling and management.

### 1.1 ros_metas module

ros2_metas is the ROS middleware node for the metaS driver, which is used to receive sensor data from metaS, integrate the data, and then publish it for use by other nodes. This includes data from three sources: camera, lidar, and IMU.



## 2. Prerequisites

### 2.1 Install ROS2

Please refer to the official [ROS 2 installation guide](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html) guidance

### 2.2 Install source code

Create `colcon` workspace

```
mkdir -p ~/ros2_humble/src
```

Get source code, and default full code,

```shell
cd ros2_humble
git clone https://github.com/RoboSense-Robotics/robosense_ac_studio.git
vcs import src < ac_studio/ac_studio.repos
```

Or to download only a specific repository, you need to modify the ac_studio.repos file of the ac_studio repository to preserve only the repository path that contains the driver.

```shell
repositories:
  ac_studio/robosense_ac_ros2_sdk_infra:
    type: git
    url: https://github.com/RoboSense-Robotics/robosense_ac_ros2_sdk_infra.git
    version: main
```



## 3. Build&Run

Please refer to the README file operation mode in each warehouse compilation and operation mode.



## 6. License
Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
