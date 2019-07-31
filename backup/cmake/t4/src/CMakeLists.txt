INCLUDE_DIRECTORIES(/home/zxy/myCode/cmake-practice/backup/cmake/t3/build/include/hello)

#另一种添加非标准include路径的方式
#需要在bash设置CMAKE_INCLUDE_PATH变量
#FIND_PATH(myHeader hello.h)
#IF(myHeader)
#		INCLUDE_DIRECTORIES(${myHeader})
#ENDIF(myHeader)

ADD_EXECUTABLE(main main.c)
#链接到动态库
#TARGET_LINK_LIBRARIES(main /home/zxy/myCode/cmake-practice/backup/cmake/t3/build/lib/libhello.so)
#链接到静态库
TARGET_LINK_LIBRARIES(main /home/zxy/myCode/cmake-practice/backup/cmake/t3/build/lib/libhello.a)
