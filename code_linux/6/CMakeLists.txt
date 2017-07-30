INCLUDE_DIRECTORIES(.)

find_package(PkgConfig)
pkg_check_modules(OPENCV REQUIRED opencv)

include_directories(${OPENCV_INCLUDE_DIRS})
link_directories(${OPENCV_LIBRARY_DIRS})
#message(${OPENCV_INCLUDE_DIRS},${OPENCV_CFLAGS},${OPENCV_CFLAGS_OTHER})
#message(${OPENCV_LIBRARIES},${OPENCV_LIBRARY_DIRS},${OPENCV_LDFLAGS},${OPENCV_LDFLAGS_OTHER})

#SET(SRC_LIST TestRtclib.cpp)
#FILE(GLOB SRC_LIST "*.cpp")

SET(SRC_LIST 31_boxFilter.cpp)
ADD_EXECUTABLE(Test31 ${SRC_LIST})
target_link_libraries(Test31 ${OPENCV_LIBRARIES})

SET(SRC_LIST 32_blur.cpp)
ADD_EXECUTABLE(Test32 ${SRC_LIST})
target_link_libraries(Test32 ${OPENCV_LIBRARIES})

SET(SRC_LIST 33_GaussianBlur.cpp)
ADD_EXECUTABLE(Test33 ${SRC_LIST})
target_link_libraries(Test33 ${OPENCV_LIBRARIES})

SET(SRC_LIST 34_LinearImageFilter.cpp)
ADD_EXECUTABLE(Test34 ${SRC_LIST})
target_link_libraries(Test34 ${OPENCV_LIBRARIES})

SET(SRC_LIST 35_medianBlur.cpp)
ADD_EXECUTABLE(Test35 ${SRC_LIST})
target_link_libraries(Test35 ${OPENCV_LIBRARIES})

SET(SRC_LIST 36_bilateralFilter.cpp)
ADD_EXECUTABLE(Test36 ${SRC_LIST})
target_link_libraries(Test36 ${OPENCV_LIBRARIES})

SET(SRC_LIST 37_ImageFiltering.cpp)
ADD_EXECUTABLE(Test37 ${SRC_LIST})
target_link_libraries(Test37 ${OPENCV_LIBRARIES})

SET(SRC_LIST 40_dilate_And_erode.cpp)
ADD_EXECUTABLE(Test40 ${SRC_LIST})
target_link_libraries(Test40 ${OPENCV_LIBRARIES})

SET(SRC_LIST 55_threshold.cpp)
ADD_EXECUTABLE(Test55 ${SRC_LIST})
target_link_libraries(Test55 ${OPENCV_LIBRARIES})
