INCLUDE_DIRECTORIES(.)

find_package(PkgConfig)
pkg_check_modules(OPENCV REQUIRED opencv)

include_directories(${OPENCV_INCLUDE_DIRS})
link_directories(${OPENCV_LIBRARY_DIRS})
#message(${OPENCV_INCLUDE_DIRS},${OPENCV_CFLAGS},${OPENCV_CFLAGS_OTHER})
#message(${OPENCV_LIBRARIES},${OPENCV_LIBRARY_DIRS},${OPENCV_LDFLAGS},${OPENCV_LDFLAGS_OTHER})

#SET(SRC_LIST TestRtclib.cpp)
#FILE(GLOB SRC_LIST "*.cpp")

SET(SRC_LIST 8_CamShiftDemo.cpp)
ADD_EXECUTABLE(Test8 ${SRC_LIST})
target_link_libraries(Test8 ${OPENCV_LIBRARIES})

SET(SRC_LIST 9_OpticalFlow.cpp)
ADD_EXECUTABLE(Test9 ${SRC_LIST})
target_link_libraries(Test9 ${OPENCV_LIBRARIES})

SET(SRC_LIST 10_lkdemo.cpp)
ADD_EXECUTABLE(Test10 ${SRC_LIST})
target_link_libraries(Test10 ${OPENCV_LIBRARIES})

SET(SRC_LIST 11_ObjectDetection.cpp)
ADD_EXECUTABLE(Test11 ${SRC_LIST})
target_link_libraries(Test11 ${OPENCV_LIBRARIES})

#SET(SRC_LIST 12_SupportVectorMachines.cpp)
#ADD_EXECUTABLE(Test12 ${SRC_LIST})
#target_link_libraries(Test12 ${OPENCV_LIBRARIES})

#SET(SRC_LIST 13_SVMForNonLinearlySeparableData.cpp)
#ADD_EXECUTABLE(Test13 ${SRC_LIST})
#target_link_libraries(Test13 ${OPENCV_LIBRARIES})
