# Catkin User Guide: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/user_guide.html
# Catkin CMake Standard: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/standards.html
cmake_minimum_required(VERSION 2.8.3)
project(collvoid_controller)

find_package(catkin REQUIRED COMPONENTS rospy std_msgs tf geometry_msgs std_srvs collvoid_local_planner)

# catkin_python_setup()
catkin_package(
    DEPENDS rospy std_msgs tf geometry_msgs std_srvs collvoid_local_planner
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS # TODO include
    LIBRARIES # TODO
)

install(PROGRAMS 
	src/collvoid_controller/active_collision_avoidance.py
	src/collvoid_controller/collvoid_visualizer.py
	src/collvoid_controller/controller.py
	src/collvoid_controller/controller_robots.py
	src/collvoid_controller/detect_obstacles.py
	src/collvoid_controller/people_tracker.py
	src/collvoid_controller/__init__.py
	src/collvoid_controller/position_share_controller.py
	src/collvoid_controller/watchdog.py
   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

