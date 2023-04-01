# cmake最小版本号
cmake_minimum_required(VERSION 3.0)

# 你所建立的工程的版本号
project(MYPROJECT VERSION 1.0.0)

# 设置语言标准
set(MAKE_C_STANDARD 99)
set(MAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# ./ 表示的是在当前目录内  ../表示的是在上一级目录下  / 表示的是在子目录内
# ${CMAKE_SOURCE_DIR} 表示当前文件所在目录的绝对地址
include_directories(${CMAKE_SOURCE_DIR}/inc)

# 查找目录下的所有源文件
# 并将名称保存到 SRC_LIST变量
aux_source_directory(./src SRC_LIST)

# add_executable(phase_one main.cpp ${SRC_LIST})
add_executable(MYPROJECT ./main.cpp ${SRC_LIST})
