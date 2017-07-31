CMAKE_MINIMUM_REQUIRED( VERSION 2.8 ) #设定版本
PROJECT(CV_net ) #设定工程名
SET( CMAKE_CXX_COMPILER "g++") #设定编译器
FIND_PACKAGE(OpenCV REQUIRED)	


#设定可执行二进制文件的目录
SET( EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin) 
	
#设定存放编译出来的库文件的目录
SET( LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib) 
#并且把该目录设为连接目录
LINK_DIRECTORIES( ${PROJECT_SOURCE_DIR}/lib)
	
#设定头文件目录
INCLUDE_DIRECTORIES( ${PROJECT_SOURCE_DIR}/include)

add_executable(CV_net main.cpp)
target_link_libraries(CV_net ${OpenCV_LIBS})
