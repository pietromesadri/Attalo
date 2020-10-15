cmake_minimum_required(VERSION 3.15)
project(Attalo VERSION 0.0.1)

find_package(OpenGL REQUIRED)
find_package(glfw3 3.3 REQUIRED)


set(GLAD "/usr/include/glad/glad.h"
         "lib/src/glad.c")

set(SOURCE_FILES "src/main.cpp" "src/displayManager.cpp"
           "src/input.cpp" "src/renderer.cpp" "src/stb_image.cpp")


add_executable(Attalo ${SOURCE_FILES} ${GLAD})

target_link_libraries(Attalo OpenGL::GL)
target_link_libraries(Attalo glfw)
target_link_libraries(Attalo dl)
