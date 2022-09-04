# OpenGL Starter Kit for C++
This is my starter kit for OpenGL 3.3+ development in C++ using GLFW and GLAD.

#### Setup

##### Unix-like
1. Install the required packages:
    ```
    sudo apt-get install cmake libxrandr-dev libxinerama-dev libxcursor-dev libxi-dev
    ```
2. Clone the repository
3. Install the submodules:
    ```
    git submodule update --init --recursive
    ```
4. Configure the project:
    ```
    scripts/configure.sh
    ```
5. Build the project:
    ```
    scripts/build.sh
    ```
6. Run the project:
    ```
    scripts/run.sh
    ```

##### Windows
Probably try building under WSL with the same steps.

#### Building
The following static libraries under `lib/` must be built (step 5) before the main project can be built:

- GLAD `lib/glad/src/glad.o`
- GLFW `lib/glfw/src/libglfw3.a`

If libraries are not found, ensure that submodules have been cloned.

Finally, the output executable will be located under `out/build`.
