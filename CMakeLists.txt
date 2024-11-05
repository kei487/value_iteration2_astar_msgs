cmake_minimum_required(VERSION 3.8)
project(ike_nav_msgs)

find_package(ament_cmake_auto REQUIRED)

ament_auto_find_build_dependencies()

rosidl_generate_interfaces(${PROJECT_NAME}
  "srv/GetPath.srv"
  DEPENDENCIES geometry_msgs nav_msgs
)

rosidl_get_typesupport_target(cpp_typesupport_target "${PROJECT_NAME}" "rosidl_typesupport_cpp")

ament_export_dependencies(rosidl_default_runtime)

ament_auto_package()
