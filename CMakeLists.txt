cmake_minimum_required(VERSION 3.14)

# Define the library name and version
project(mylib VERSION 1.0.0)

# Define the source files
set(SOURCES src/mylib.cpp)

# Define the header files
set(HEADERS include/mylib.h)

# Create a static library target
add_library(mylib STATIC ${SOURCES} ${HEADERS})

# Specify the include directories for the library target
target_include_directories(mylib PUBLIC include)

# Specify the installation rules for the library target
install(TARGETS mylib DESTINATION lib)
install(FILES ${HEADERS} DESTINATION include)