cmake_minimum_required(VERSION 3.29.0)
project(planning
VERSION 0.0.1
DESCRIPTION "a demo of cmake planning"
HOMEPAGE_URL "https://github.com/ct6129/mult_cmake_test"
LANGUAGES CXX
)
set(CMAKE_CXX_STANDARD 17)
#将lib和可执行文件都放在bin目录下
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
# 在父类中定义变量，子类也可以用到
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process)
set(PNC_MAP_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map)
# 添加子目录,实际上找到src下的CMakeLists.txt
add_subdirectory(src)