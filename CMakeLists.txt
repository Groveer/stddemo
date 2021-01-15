cmake_minimum_required(VERSION 3.7)

project(stddemo CXX)

set(BIN_NAME stddemo)

set(CMAKE_CXX_STANDARD_REQUIRED 20)

# Install settings
if(NOT DEFINED CMAKE_INSTALL_PREFIX)
    set(CMAKE_INSTALL_PREFIX /usr)
endif()

file(GLOB_RECURSE SRCS
    "src/*.h"
    "src/*.cpp"
)

add_executable(${BIN_NAME}
    ${SRCS}
)

target_include_directories(${BIN_NAME} PUBLIC
)

target_link_libraries(${BIN_NAME} PRIVATE
)

install(TARGETS ${BIN_NAME} DESTINATION bin)

