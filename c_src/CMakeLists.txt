# Klein C-bindings

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -msse4.1")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -msse4.1")

add_library(klein_c klein_c.cpp)
target_link_libraries(klein_c PRIVATE klein)
target_compile_features(klein_c PRIVATE cxx_std_11)