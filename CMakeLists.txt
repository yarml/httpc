cmake_minimum_required(VERSION 3.12)

project(httpc)

file(GLOB_RECURSE SRC_FILES "src/*.c")
file(GLOB_RECURSE INC_FILES "inc/*.h" "src/*.h")

set(HTTPC "httpc")

add_executable(
  ${HTTPC}
  ${SRC_FILES}
  ${INC_FILES}
)

target_include_directories(
  ${HTTPC}
  PUBLIC "inc/"
)