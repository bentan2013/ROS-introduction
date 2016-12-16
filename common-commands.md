---
title: ROS常用命令
tags: []
notebook: ros
---

* 配置账户需要输入的
    <div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rosdep update</div>

  





* 将ros包的环境加入到当前控制台




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

source ./devel/setup.bash

</div>

  





* 将ros环境加入到当前控制台的环境变量




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

source /opt/ros/indigo/setup.bash

</div>

  


* 获取所有已安装ROS软件包列表清单




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rospack list

</div>

  





* 编译




<div markdown="1" style="box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, 'Courier New', monospace; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902);">

catkin_make

catkin_make install

</div>

  





* 看依赖
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

rospack depends1 beginner_tutorials</div>

* 切到包中
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

$ roscd beginner_tutorials

</div>

* 编译工程
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

catkin_make </div>

* 输出包的安装目录
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

$ pwd</div>

* 运行核心程序
    <div markdown="1" style="box-sizing: border-box; display: block; padding: 5pt; margin: 0px 0px 10px; border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

$ roscore

</div>

<div markdown="1" style="box-sizing: border-box; font-weight: 500; margin-top: 10px; margin-bottom: 10px; font-style: normal; font-variant: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; white-space: normal; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(255, 255, 255);">

*   turtlesim的例子


    $ rosrun turtlesim turtlesim_node



​    
​    
    $ rosrun turtlesim turtle_teleop_key
​    

<div markdown="1" style="box-sizing: border-box; list-style-type: none;">

  


*   查看当前系统运行情况的动态图形


    $ rosrun rqt_graph rqt_graph




* 获取特定节点的信息




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rosnode info node-name

</div>

  


* 完全删除已经运行完毕节点的记录




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rosnode cleanup

</div>

  





* 查看在某个话题上发布的数据
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

rostopic echo [topic]  
</div>

</div>

示例代码：
​    
​    
    $ rostopic echo /turtle1/cmd_vel
​    

  


* 列出当前发布的话题
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

rostopic list -v

</div>

* 查看更多信息




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rostopic info topic-name

</div>

  


* 使用命令行发布数据




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rostopic pub -r rate-in-hz topic-name message-type message content

</div>

  





</div>

* 查看消息类型
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

$ rostopic type /turtle1/cmd_vel</div>

你应该会看到:

<div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: left; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

geometry_msgs/Twist  
</div>

  


*   查看消息的详细情况


    $ rosmsg show geometry_msgs/Twist

*   <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(243, 245, 247);">

geometry_msgs/Vector3 linear  
float64 x  
float64 y  
float64 z  
geometry_msgs/Vector3 angular  
float64 x  
float64 y  
float64 z  
</div>

  


* 将数据发布到某个正在广播的话题上
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

rostopic pub [topic] [msg_type] [args]  
</div>

  


* 查看发布到某个话题上面的图形
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

$ rosrun rqt_plot rqt_plot  
</div>

  


* 服务相关
    <div markdown="1" style="box-sizing: border-box; font-family: courier, monospace; display: block; padding: 5pt; margin: 0px 0px 10px; color: rgb(51, 51, 51); border: 1pt solid rgb(174, 189, 204); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; orphans: auto; text-align: start; text-indent: 0px; text-transform: none; widows: 1; word-spacing: 0px; -webkit-text-stroke-width: 0px; background-color: rgb(243, 245, 247);">

rosservice list 输出可用服务的信息  
rosservice call 调用带参数的服务  
rosservice type 输出服务类型  
rosservice find 依据类型寻找服务find services by service type  
rosservice uri 输出服务的ROSRPC uri  
</div>

  


* **录制**




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rosbag info NAME

rosbag play NAME

</div>

  


* 问题检查




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

roswtf

</div>

  


* 创建功能包
    <div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

catkin_create_pkg package-name

</div>

  


* 查看/rosout消息




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rqt_console

</div>

  


* 在roslaunch中请求输出详细信息




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

roslaunch -v package-name launch-file-name

</div>

  


* 在控制台中设置所有节点的输出




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

roslaunch -screen package-name launch-file-name

</div>

  


* 新窗口中显示数据




<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

加入前缀， launch-prefix=“xetrm-e”

xterm -e rosrun package node

</div>

  


* 更换节点名




  


<div markdown="1" style="-en-codeblock: true; box-sizing: border-box; padding: 8px; font-family: Monaco, Menlo, Consolas, "Courier New", monospace; font-size: 12px; color: rgb(51, 51, 51); border-top-left-radius: 4px; border-top-right-radius: 4px; border-bottom-right-radius: 4px; border-bottom-left-radius: 4px; background-color: rgb(251, 250, 248); border: 1px solid rgba(0, 0, 0, 0.14902); background-position: initial initial; background-repeat: initial initial;">

rosrun turtlesim turtlesim_node turtle1/pos:=tim

<remap from="org-name"to "new-name">

</div>

  





  





End

  

