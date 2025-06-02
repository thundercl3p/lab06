cmake_minimum_required(VERSION 3.10)

project(solver-pckg VERSION 0.1.17 LANGUAGES C CXX)

set(PRINT_VERSION ${PROJECT_VERSION})

add_subdirectory(solver_application)
add_subdirectory(hello_world_application)

install(TARGETS solver_app
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib
)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPackConfig.cmake)
