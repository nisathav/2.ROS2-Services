# 2.ROS2-Services
Services are there to bring the architecture of request and response like client and server operation

ROS2 commands,
1. ros2 run demo_nodes_cpp add_two_ints_server
2. ros2 service list #another terminal
3. ros2 node list - add_two_ints_server will the output
4. ros2 service type /add_two_ints
5. ros2 interface show <above_output_4>
6. ros2 service call /add_two_ints <output_4> "{'a':4,'b':5}" #this code generate a request with input of 4 and 5 for a and b respectively also generates the response
   (output will be there on another terminal on code 1)(another terminal)

Analyze turtlesim
1. ros2 run turtlesim turtlesim_node
2. ros2 service list #at
3. ros2 service type /turtle1/set_pen turtlesim/srv/SetPen #used to change the color of the line drawn by the turtle
4. ros2 interface show turtlesim/srv/SetPen
5. ros2 service call /turtle1_set_pen turtlesim/srv/SetPen "{'r':255, 'g':0, 'b':0, 'width':6, 'off':0}"

if we kill th turtlesim and try to sent the request the output will be 'waiting for the service to become available'
