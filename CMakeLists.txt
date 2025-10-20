cmake_minimum_required(VERSION 3.11)
project(PBNotes)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -stdlib=libc++")
#set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -stdlib=libc++")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# GCC 15 stdlib
set(GCC15_INCLUDE_DIRS "/usr/include/c++/15" "/usr/include/x86_64-linux-gnu/c++/15")
set(GCC15_LIB_DIR "/usr/lib/gcc/x86_64-linux-gnu/15")

add_compile_options(
    -isystem ${GCC15_INCLUDE_DIRS}
)

link_directories(${GCC15_LIB_DIR})
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -Wl,-rpath,${GCC15_LIB_DIR}")

add_subdirectory(src)
add_subdirectory(test)