# fssim 组织架构解析

## 简介

fssim 通过 gazebo 完成复杂的模拟工作，之后通过 rviz 将结果输出。

## 架构解析

fssim_common 主要用于放置自定义的msg文件
fssim_description 用于定义车辆性质及赛道
fssim_gazebo包含：  

- meshes 有锥桶和激光雷达的“材质”文件
- models 定义了各颜色的锥桶及赛道的几何模型（包括模拟太阳光照；计时设备；地平面）
    - track （赛道）使用 sdf （类xml）定义赛道锥桶位置
    - cone_* 定义各种颜色锥桶
    - ...
- worlds 下定义了用于gazebo模拟的世界参数设计

# 参考链接
https://zhuanlan.zhihu.com/p/129660662