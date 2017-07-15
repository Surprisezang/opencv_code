INCLUDE_DIRECTORIES(.)

find_package(PkgConfig)
pkg_check_modules(OPENCV REQUIRED opencv)

include_directories(${OPENCV_INCLUDE_DIRS})
link_directories(${OPENCV_LIBRARY_DIRS})
#message(${OPENCV_INCLUDE_DIRS},${OPENCV_CFLAGS},${OPENCV_CFLAGS_OTHER})
#message(${OPENCV_LIBRARIES},${OPENCV_LIBRARY_DIRS},${OPENCV_LDFLAGS},${OPENCV_LDFLAGS_OTHER})

#SET(SRC_LIST TestRtclib.cpp)
#FILE(GLOB SRC_LIST "*.cpp")

SET(SRC_LIST 1_HelloOpenCV.cpp)
ADD_EXECUTABLE(Test1 ${SRC_LIST})
target_link_libraries(Test1 ${OPENCV_LIBRARIES})

SET(SRC_LIST 2_ShowImage.cpp)
ADD_EXECUTABLE(Test2 ${SRC_LIST})
target_link_libraries(Test2 ${OPENCV_LIBRARIES})

SET(SRC_LIST 3_ImageErode.cpp)
ADD_EXECUTABLE(Test3 ${SRC_LIST})
target_link_libraries(Test3 ${OPENCV_LIBRARIES})

SET(SRC_LIST 4_BlurImage.cpp)
ADD_EXECUTABLE(Test4 ${SRC_LIST})
target_link_libraries(Test4 ${OPENCV_LIBRARIES})

SET(SRC_LIST 5_Canny.cpp)
ADD_EXECUTABLE(Test5 ${SRC_LIST})
target_link_libraries(Test5 ${OPENCV_LIBRARIES})

SET(SRC_LIST 6_PlayVideo.cpp)
ADD_EXECUTABLE(Test6 ${SRC_LIST})
target_link_libraries(Test6 ${OPENCV_LIBRARIES})

SET(SRC_LIST 7_UseCamera.cpp)
ADD_EXECUTABLE(Test7 ${SRC_LIST})
target_link_libraries(Test7 ${OPENCV_LIBRARIES})
