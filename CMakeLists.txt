cmake_minimum_required(VERSION 3.10)
project(github_action_ccache VERSION 0.1.0 LANGUAGES CXX)

add_executable(main src/main.cpp)

install(TARGETS main
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib)

install(FILES package.xml DESTINATION share/${PROJECT_NAME})

enable_testing()
add_test(NAME main COMMAND main)
