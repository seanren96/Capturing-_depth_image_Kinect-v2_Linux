CMAKE_MINIMUM_REQUIRED(VERSION 2.8.12)
PROJECT(FREE)

SET(DEPENDS_DIR "/home/odroid/libfreenect2/depends")
SET(MY_DIR "/home/odroid/Desktop/libfreenect2")
# CONFIGURE OPENCV
find_package(OpenCV REQUIRED)
find_package(freenect2 REQUIRED)

#set the default path for built executables to the "bin" directory
SET(EXECUTABLE_OUTPUT_PATH ${MY_DIR}/bin)
ADD_EXECUTABLE(test test.cpp)
  
target_link_libraries(test  ${OpenCV_LIBS}
                            ${freenect2_LIBRARIES})

