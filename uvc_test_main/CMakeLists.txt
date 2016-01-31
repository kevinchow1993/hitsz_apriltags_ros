cmake_minimum_required(VERSION 2.8.3)
project(uvc_apriltags_test)

find_package( OpenCV REQUIRED )

find_package(catkin REQUIRED COMPONENTS
  cv_bridge
  image_transport
  roscpp
  std_msgs
  uvc_camera
)


catkin_package(

)


include_directories(
  include
  ${catkin_INCLUDE_DIRS}
  ${OpenCV_INCLUDE_DIRS}
)


add_executable(result_subscriber src/result_subscriber.cpp)
target_link_libraries(result_subscriber ${catkin_LIBRARIES} ${OpenCV_LIBRARIES})


