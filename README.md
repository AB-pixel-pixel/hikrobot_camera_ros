# hikrobot_camera

让海康相机输出ROS的rgb图像

## 目录

- [hikrobot_camera](#hikrobot_camera)
  - [目录](#目录)
  - [背景](#背景)
  - [环境准备](#环境准备)
    - [安装海康威视SDK](#安装海康威视sdk)
    - [下载并编译](#下载并编译)
  - [运行代码](#运行代码)
  - [使用说明](#使用说明)
  - [TODO](#todo)
  - [相关仓库](#相关仓库)
  - [维护者](#维护者)
  - [如何贡献](#如何贡献)

## 背景


## 环境准备
- 环境：
  - ubuntu20.04
  - ros noteic
  - 海康威视SDK V3.2.0


### 安装海康威视SDK
1. [海康威视资料中心](https://www.hikrobotics.com/cn/machinevision/service/download?module=0)
2. 找到工业相机SDK V3.2.0(Linux)
3. 安装时，注意芯片架构。可选择deb包安装。
### 下载并编译

```
mkdir -p ~/hik_camera_ws/src
cd ~/hik_camera_ws/src
git clone https://github.com/AzureSpace531/hikrobot_camera ~/hik_camera_ws/src/hikrobot_camera
cd ~/hik_camera_ws
catkin_make
```


## 运行代码
launch run

```
source ./devel/setup.bash 
roslaunch hikrobot_camera hikrobot_camera.launch
```

use rviz subscribe topic： /hikrobot_camera/rgb

```
source ./devel/setup.bash 
roslaunch hikrobot_camera hikrobot_camera_rviz.launch
```

## 使用说明
我主要是对着几份代码，修改了一下cmake，让代码跑通。待我细读之后，再说明。

## TODO
- [ ] 支持相机标定
- [ ] 支持多相机


## 相关仓库

- [主要参照的仓库](https://github.com/luckyluckydadada/HIKROBOT-MVS-CAMERA-ROS),目前整体代码来源于此仓库
- [次要参照的仓库](https://github.com/WhiteCri/hikrobot_multicam_ros),观察了一下本地SDK文件然后参照本仓库进行cmake的修改


## 维护者

- [Bin](https://github.com/AB-pixel-pixel)


## 如何贡献

提一个 Issue或者提交一个 Pull Request


