
###Ros source list

/ect/apt/sources.list/ros-latest.lis

###Source Space

The source space contains the source code of catkin packages. This is where you can extract/checkout/clone source code for the packages you want to build. Each folder within the source space contains one or more catkin packages. This space should remain unchanged by configuring, building, or installing. The root of the source space contains a symbolic link to catkin's boiler-plate 'toplevel' CMakeLists.txt file. This file is invoked by CMake during the configuration of the catkin projects in the workspace. It can be created by calling catkin_init_workspace in the source space directory.



###Build Space

The build space is where CMake is invoked to build the catkin packages in the source space. CMake and catkin keep their cache information and other intermediate files here. The build space does not have to be contained within the workspace nor does it have to be outside of the source space, but this is recommended.

build 目录是build space的默认所在位置，同时cmake 和 make也是在这里被调用来配置并编译你的程序包。

###Development (Devel) Space

The development space (or devel space) is where built targets are placed prior to being installed. The way targets are organized in the devel space is the same as their layout when they are installed. This provides a useful testing and development environment which does not require invoking the installation step. The location of the devel space is controlled by a catkin specific CMake variable called CATKIN_DEVEL_PREFIX, and it defaults to<build space>/develspace. This is the default behavior because it might be confusing to CMake users if they invokedcmake .. in a build folder and that modified things outside of the current directory. It is recommended, however, to set thedevel space directory to be a peer of the build space directory.

devel 目录是devel space的默认所在位置, 同时也是在你安装程序包之前存放可执行文件和库文件的地方。

###Install Space

Once targets are built, they can be installed into the install space by invoking the install target, usually with make install. The install space does not have to be contained within the workspace. Since the install space is set by theCMAKE_INSTALL_PREFIX, it defaults to /usr/local, which you should not use (because uninstall is near-impossible, and using multiple ROS distributions does not work either).



###Result space

When ever referring to a folder which can either be a development space or an install space the generic term result spaceis used.



###ros包的位置

/opt/ros/kinetic/share/turtlesim


###自己编写的节点的生成位置

这会生成两个可执行文件, talker 和 listener, 默认存储到devel space目录,具体是在~/catkin_ws/devel/lib/<package name>中.


###环境变量

`ROS_ROOT` /opt/ros/kinetic/share/ros
`ROS_PACKAGE_PATH` /opt/ros/kinetic/share
`PYTHONPATH` /opt/ros/kinetic/lib/python2.7/dist-packages


###msg生成的编程语言版本的文件的路径

所有在msg路径下的.msg文件都将转换为ROS所支持语言的源代码。生成的C++头文件将会放置在~/catkin_ws/devel/include/beginner_tutorials/。 Python脚本语言会在~/catkin_ws/devel/lib/python2.7/dist-packages/beginner_tutorials/msg 目录下创建。 lisp文件会出现在~/catkin_ws/devel/share/common-lisp/ros/beginner_tutorials/msg/ 路径下.


###The use of each folder in ROS package
- config: All configuration files that are used in this ROS package are kept in this
folder. This folder is created by the user and is a common practice to name the folder
config to keep the configuration files in it.

- include/package_name: This folder consists of headers and libraries that we need to
use inside the package.

- scripts: This folder keeps executable Python scripts. In the block diagram, we can
see two example scripts.

- src: This folder stores the C++ source codes. We can see two examples of the source
code in the block diagram.

- launch: This folder keeps the launch files that are used to launch one or more ROS
nodes.

- msg: This folder contains custom message definitions.

- srv: This folder contains the service definitions.

- action: This folder contains the action definition. We will see more about actionlib
in the upcoming sections.

- package.xml: This is the package manifest file of this package.

- CMakeLists.txt: This is the CMake build file of this package.


##REF

- http://wiki.ros.org/cn/ROS/

- “Mastering ROS for Robotics Programming(PACKT, 2015).pdf”
