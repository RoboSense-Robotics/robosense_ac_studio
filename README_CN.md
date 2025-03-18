[README](http://10.10.0.20/super_sensor_sdk/ros2_sdk/sdk_infra/-/blob/main/README.md)  \- English Version of the README

## 1. 简介

该仓库，主要存放AC1超级传感器repo多仓管理仓库文件，通过该仓库可以全量拉取AC_Studio提供的驱动、算法、工具等仓库，方便仓库拉取与管理。

## 2. 前置条件

### 2.1 下载ROS2

请参考ROS2官方的安装指南[[ROS 2 installation guide](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html)]

### 2.2 下载AC_Studio

创建`colcon`工作空间

```
mkdir -p ~/ros2_humble/src
```

获取源代码，默认全量代码，

```shell
cd ros2_humble
git clone https://github.com/RoboSense-Robotics/robosense_ac_studio.git
vcs import src < ac_studio/ac_studio.repos
```

或者只下载特定的仓库，需要修改ac_studio 仓库的ac_studio.repos文件，只保留包含驱动的仓库路径。

```shell
repositories:
  ac_studio/robosense_ac_ros2_sdk_infra:
    type: git
    url: https://github.com/RoboSense-Robotics/robosense_ac_ros2_sdk_infra.git
    version: main
```

## 3. 构建&运行

请参照各个仓库中README文件操作方式编译与运行



## 6. License
Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
