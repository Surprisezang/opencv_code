INCLUDE_DIRECTORIES(.)

find_package(PkgConfig)
pkg_check_modules(OPENCV REQUIRED opencv)

include_directories(${OPENCV_INCLUDE_DIRS})
link_directories(${OPENCV_LIBRARY_DIRS})
#message(${OPENCV_INCLUDE_DIRS},${OPENCV_CFLAGS},${OPENCV_CFLAGS_OTHER})
#message(${OPENCV_LIBRARIES},${OPENCV_LIBRARY_DIRS},${OPENCV_LDFLAGS},${OPENCV_LDFLAGS_OTHER})

#SET(SRC_LIST TestRtclib.cpp)
#FILE(GLOB SRC_LIST "*.cpp")

SET(SRC_LIST 21_UsePointerAccessPixel.cpp)
ADD_EXECUTABLE(Test21 ${SRC_LIST})
target_link_libraries(Test21 ${OPENCV_LIBRARIES})

SET(SRC_LIST 25_ImageBlending.cpp)
ADD_EXECUTABLE(Test25 ${SRC_LIST})
target_link_libraries(Test25 ${OPENCV_LIBRARIES})
