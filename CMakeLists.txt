cmake_minimum_required(VERSION 3.10)

project(solver VERSION 0.1.18 LANGUAGES C CXX)

add_subdirectory(solver_application)
add_subdirectory(hello_world_application)

install(TARGETS solver_app
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib
)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
