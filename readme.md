Copyright 2025 国地共建人形机器人创新中心/人形机器人（上海）有限公司, https://www.OpenLoong.net/

# 简介

本仓库为OpenLoong控制框架各子组件目录。

OpenLoong特点：

* **完整且独立**：除与内核绑定的IGH ethercat主站外，自集成全部运行依赖，无需任何繁琐的环境依赖配置即可跑起机器人，离线测试、仿真验证、实机运行，具备完整功能的机器人控制程序库
* **干净而朴素**：免安装，免配环境，对系统零污染，ROS free，朴素c++实现，高性能通信与任务执行
* **隔离亦统一**：模块化开发，严封装，零飞针，功能易拓展，快速满足不同机器人平台间组合或移植。仿真-实机接口、操作一致，跨平台架构，一套代码完成验证+部署

# OpenLoong控制框架

![img](./img/框架.jpg)

OpenLoong包含：

#### · [loong_utility:](https://github.com/tryingfly/loong_utility.git)

  作为公共库，提供对c++的功能库拓展，与控制无关。包含常用算法、矩阵、打印、读取配置文件、计时、udp、log等功能。

#### · [loong_ctrl_locomotion:](https://github.com/tryingfly/loong_ctrl_locomotion.git)

  loco作为上层控制框架，由状态机调度运动控制算法（可控全身关节），生成跨环境的动态库。

#### · [loong_base:](https://github.com/tryingfly/loong_base.git)

  作为控制业务主程序，生成各个组件库调用的可执行文件。

#### · [loong_sim:](https://github.com/tryingfly/loong_sim.git)

  作为仿真环境。可独立验证loco、mani算法仿真，以及作为虚拟驱动底层联合loong_base作全链仿真。

#### · [loong_sim_sdk_release:](https://github.com/tryingfly/loong_sim_sdk_release.git)

  已编译好的全链仿真sdk，模拟实机运行流程，附python调用接口示例。

#### · [loong_deploy:](https://github.com/tryingfly/loong_deployment.git)

  已编译好的部署框架文件，拷贝到实机即可运行。

### 以上仓库按需下载即可，无需全部。

各链接均为独立仓库。若使用vscode同时打开会导致智能补全功能失效。

### 另：

* [交叉编译环境配置.md](交叉编译环境.md)
* vsode部分配置.json
