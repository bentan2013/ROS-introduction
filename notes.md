## Structure



 ![ROS-Graph-layer-structure](img\ROS-Graph-layer-structure.jpg)

The following are abstracts of each graph’s concepts:


- **Nodes**: Nodes are the process that perform computation. Each ROS node is written

using ROS client libraries such as roscpp and rospy. Using client library APIs, we
can implement different types of communication methods in ROS nodes. In a robot,
there will be many nodes to perform different kinds of tasks. Using the ROS
communication methods, it can communicate with each other and exchange data.
One of the aims of ROS nodes is to build simple processes rather than a large process
with all functionality. Being a simple structure, ROS nodes are easy to debug too.
Master: The ROS Master provides name registration and lookup to the rest of the
nodes. Nodes will not be able to find each other, exchange messages, or invoke
services without a ROS Master. In a distributed system, we should run the master on
one computer, and other remote nodes can find each other by communicating with
this master.



- **Parameter Server:** The parameter server allows you to keep the data to be stored in

a central location. All nodes can access and modify these values. Parameter server is
a part of ROS Master



- **Messages:** Nodes communicate with each other using messages. Messages are

simply a data structure containing the typed field, which can hold a set of data and
that can be sent to another node. There are standard primitive types (integer, floating
point, Boolean, and so on) and these are supported by ROS messages. We can also
build our own message types using these standard types.


- **Topics:** Each message in ROS is transported using named buses called topics. When

a node sends a message through a topic, then we can say the node is publishing a
topic. When a node receives a message through a topic, then we can say that the node
is subscribing to a topic. The publishing node and subscribing node are not aware of
each other’s existence. We can even subscribe a topic that might not have any
publisher. In short, the production of information and consumption of it are
decoupled. Each topic has a unique name, and any node can access this topic and
send data through it as long as they have the right message type.


- **Services:** In some robot applications, a publish/subscribe model will not be enough if

it needs a request/response interaction. The publish/subscribe model is a kind of oneway
transport system and when we work with a distributed system, we might need a
request/response kind of interaction. ROS Services are used in these case. We can
define a service definition that contains two parts; one is for requests and the other is
for responses. Using ROS Services, we can write a server node and client node. The
server node provides the service under a name, and when the client node sends a
request message to this server, it will respond and send the result to the client. The
client might need to wait until the server responds. The ROS service interaction is
like a remote procedure call.


- **Bags:** Bags are a format for saving and playing back ROS message data. Bags are an

important mechanism for storing data, such as sensor data, which can be difficult to
collect but is necessary for developing and testing robot algorithms. Bags are very
useful features when we work with complex robot mechanisms.