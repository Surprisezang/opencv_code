INCLUDE_DIRECTORIES(.)

find_package(PkgConfig)
pkg_check_modules(OPENCV REQUIRED opencv)

include_directories(${OPENCV_INCLUDE_DIRS})
link_directories(${OPENCV_LIBRARY_DIRS})
#message(${OPENCV_INCLUDE_DIRS},${OPENCV_CFLAGS},${OPENCV_CFLAGS_OTHER})
#message(${OPENCV_LIBRARIES},${OPENCV_LIBRARY_DIRS},${OPENCV_LDFLAGS},${OPENCV_LDFLAGS_OTHER})

#SET(SRC_LIST TestRtclib.cpp)
#FILE(GLOB SRC_LIST "*.cpp")

SET(SRC_LIST 56_canny.cpp)
ADD_EXECUTABLE(Test56 ${SRC_LIST})
target_link_libraries(Test56 ${OPENCV_LIBRARIES})

SET(SRC_LIST 65_remap.cpp)
ADD_EXECUTABLE(Test65 ${SRC_LIST})
target_link_libraries(Test65 ${OPENCV_LIBRARIES})

SET(SRC_LIST 67_AffineTransform.cpp)
ADD_EXECUTABLE(Test67 ${SRC_LIST})
target_link_libraries(Test67 ${OPENCV_LIBRARIES})

SET(SRC_LIST 68_equalizeHist.cpp)
ADD_EXECUTABLE(Test68 ${SRC_LIST})
target_link_libraries(Test68 ${OPENCV_LIBRARIES})
