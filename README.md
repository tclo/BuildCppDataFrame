# BuildCppDataFrame
Build C++ DataFrame
# Install DataFrame:
    1. mkdir build
    2. cd build
    3. cmake -DCMAKE_BUILD_TYPE=Release -DHMDF_BENCHMARKS=1 -DHMDF_EXAMPLES=1 -DHMDF_TESTING=0 -DCMAKE_INSTALL_PREFIX=C:/lib/DataFrame -G"MinGW Makefiles" ..
    4. make 
    5. make install 

# Build exampe: 
    1. cd examples
    2. mkdir build
    3. cd build
    4. cmake -G"MinGW Makefiles" -D CMAKE_BUILD_TYPE="Debug" ..   
    5. make 
    6. .\hello_world.exe

# Git command:
    1. git config --global user.email "tclo@livemail.tw"
    2. git config --global user.name T.C.Luo
    3. git status
    4. git add .
    5. git commit -m <title> -m <description>
       git commit -m ‘Try’
    6. git push