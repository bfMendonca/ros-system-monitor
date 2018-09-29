cmake_minimum_required(VERSION 2.8.3)
project(system_monitor)

find_package(catkin REQUIRED COMPONENTS message_generation rospy)

catkin_python_setup()

catkin_package(
  CATKIN_DEPENDS message_runtime
)

catkin_install_python( PROGRAMS bin/cpu_monitor.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

catkin_install_python( PROGRAMS bin/hdd_monitor.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

catkin_install_python( PROGRAMS bin/mem_monitor.py 
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

catkin_install_python( PROGRAMS bin/net_monitor.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

catkin_install_python( PROGRAMS bin/ntp_monitor.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})  