cmake_minimum_required(VERSION 2.8.3)
project(test_store)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  mongodb_store roscpp geometry_msgs
)


catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)



# Declare a cpp executable
add_executable(example_mongodb_store_cpp_client src/example_mongodb_store_cpp_client.cpp)


# Specify libraries to link a library or executable target against
target_link_libraries(example_mongodb_store_cpp_client
  ${catkin_LIBRARIES}
)


message(${catkin_LIBRARIES})