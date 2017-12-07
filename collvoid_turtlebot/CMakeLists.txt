cmake_minimum_required(VERSION 2.8.3)
project(collvoid_turtlebot)
find_package(catkin REQUIRED )

catkin_package(
    DEPENDS # TODO add dependencies
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS # TODO include
    LIBRARIES # TODO
)

install(PROGRAMS
        scripts/lcm_relay_share.py
        scripts/lcm_ros_relay.py
        scripts/make_goals.py
   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY
    launch/
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)

install(DIRECTORY
    params/
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/params
)

install(DIRECTORY
    map/
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/map
)

install(DIRECTORY
    world/
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/world
)
