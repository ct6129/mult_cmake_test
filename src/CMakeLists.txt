project(planning_main)
add_subdirectory(pnc_map)
add_subdirectory(process)
# 可执行文件
add_executable(${PROJECT_NAME} planning_main.cpp)
# 添加头文件
target_include_directories(${PROJECT_NAME}
PUBLIC
${Process_Dir}
)
target_link_libraries(${PROJECT_NAME}
PUBLIC
process
)
 