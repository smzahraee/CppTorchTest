cmake_minimum_required(VERSION 3.10)
project(TorchExample)

# Set the C++ standard to C++17
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED YES)

# Find the Torch package
find_package(Torch REQUIRED)

# Add the executable
add_executable(TorchExample main.cpp)

# Link the Torch library
target_link_libraries(TorchExample "${TORCH_LIBRARIES}")

# Set the path to include the necessary Torch headers
target_include_directories(TorchExample PRIVATE "${TORCH_INCLUDE_DIRS}")

# Add CXX flags for compiling with PyTorch
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${TORCH_CXX_FLAGS}")

