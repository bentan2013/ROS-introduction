---
title: ROS常用命令
tags: []
notebook: ros

---



配置账户需要输入的

rosdep update



将ros包的环境加入到当前控制台
`source ./devel/setup.bash`

将ros环境加入到当前控制台的环境变量
`source /opt/ros/indigo/setup.bash`


获取所有已安装ROS软件包列表清单
`rospack list`

编译
`catkin_makecatkin_make install`

看依赖

`rospack depends1 beginner_tutorials`



切到包中

`$ roscd beginner_tutorials`

编译工程

`catkin_make`

输出包的安装目录

`$ pwd`

运行核心程序

`$ roscoreturtlesim的例子`$ rosrun turtlesim turtlesim_node`
`$ rosrun turtlesim turtle_teleop_key`

查看当前系统运行情况的动态图形

`$ rosrun rqt_graph rqt_graph`


获取特定节点的信息
`rosnode info node-name`


完全删除已经运行完毕节点的记录
`rosnode cleanup`

查看在某个话题上发布的数据

`rostopic echo [topic]`
示例代码：

`$ rostopic echo /turtle1/cmd_vel`


列出当前发布的话题

`rostopic list -v`

查看更多信息
`rostopic info topic-name`


使用命令行发布数据
`rostopic pub -r rate-in-hz topic-name message-type message content`

查看消息类型

`$ rostopic type /turtle1/cmd_vel`

`你应该会看到:geometry_msgs/Twist`

查看消息的详细情况

`$ rosmsg show geometry_msgs/Twist`

```
geometry_msgs/Vector3 linear

  float64 x

  float64 y

  float64 z

geometry_msgs/Vector3 angular

  float64 x

  float64 y

  float64 z
```



将数据发布到某个正在广播的话题上

`rostopic pub [topic][msg_type] [args]`

查看发布到某个话题上面的图形

`$ rosrun rqt_plot rqt_plot`

服务相关

```
rosservice list         输出可用服务的信息

rosservice call         调用带参数的服务

rosservice type         输出服务类型

rosservice find         依据类型寻找服务find services by service type

rosservice uri          输出服务的ROSRPC uri

```



录制
`rosbag info NAMErosbag play NAME`


问题检查
`roswtf`


创建功能包 

`catkin_create_pkg package-name`


查看/rosout消息
`rqt_console`


在roslaunch中请求输出详细信息
`roslaunch -v package-name launch-file-name`


在控制台中设置所有节点的输出
`roslaunch -screen package-name launch-file-name`


新窗口中显示数据
`加入前缀， launch-prefix=“xetrm-e”xterm -e rosrun package node`


更换节点名

`rosrun turtlesim turtlesim_node turtle1/pos:=tim<remap from="org-name"to "new-name">`



