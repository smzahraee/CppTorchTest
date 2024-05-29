# PyTorch C++ Example in Linux

## Overview

This project is a C++ application that utilizes the PyTorch library for machine learning and neural network operations. The following instructions will guide you through setting up the necessary environment and building the project.
Prerequisites

- C++ Compiler (e.g., g++, clang++) c++ 17 support required
- CMake (version 3.10 or higher)

## Setup Instructions

1. Download PyTorch C++ Library 

    Visit the PyTorch Get Started page.[Link](https://pytorch.org/get-started/locally/)
    
    Select the options for your environment:

        Compute Platform: CPU
        Language: C++
        Package: LibTorch
        Download the ZIP file.

    ![alt text](<torch.png>)
2. Extract the PyTorch Library

    Unzip the downloaded file to your desired path. For instance, you can extract it to /path/to/libtorch.

3. Build the Project

    Follow these steps to build the project:

    ```bash
    git clone https://github.com/smzahraee/CppTourchTest.git
    cd CppTourchTest
    mkdir build && cd build
    cmake -DCMAKE_PREFIX_PATH=/path/to/libtorch ../
    make -j4
    ```

### Troubleshooting

- Ensure that the CMAKE_PREFIX_PATH is correctly set to the path where you extracted the PyTorch library.
- Make sure that you have the correct version of CMake (3.10 or higher).
- Check that your C++ compiler is installed and properly configured.
- Make sure you set c++ version to 17.