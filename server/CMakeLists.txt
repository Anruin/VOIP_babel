find_package(Threads)

include_directories(${CMAKE_INCLUDE_PATH})
include_directories(include)

file(GLOB SOURCES "src/*.cpp")
file(GLOB INCLUDES "include/*.h")

add_executable(server ${SOURCES} ${INCLUDES})

target_link_libraries (server ${CMAKE_THREAD_LIBS_INIT})