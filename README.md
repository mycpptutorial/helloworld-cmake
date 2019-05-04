# helloworld-cmake

This sample is showing you how you can use cmake and CMakeLists.txtfile to compile your c++ application.

## Environment Setup

Make sure **g++** installed. If not go to http://kabiliravi.com/index.php/software/programming/mycpptutorial/environment-setup/build-and-run-your-first-application-with-gcc/ for more help.

Also make sure **make** command is intalled. If not go to http://kabiliravi.com/index.php/software/programming/mycpptutorial/environment-setup/build-and-run-your-first-application-with-make/ for more help.

Run following command to see if **cmake** is installed:

```
$ cmake --version
zsh: command not found: cmake
```
If you face **command not found: cmake** that means it is not there.

### Installing make

  - MacOS
    ```
    $ brew install cmake
    ```
  - Linux
    - Debian/Ubuntu
      ```
      $ sudo apt install cmake
      ```

## Building Hello World application

Create a folder called *build* and then use *cmake* command to build the application. It uses Makefile compile the sources to object files.

```
$ mkdir build
$ cd build
$ cmake .. -DCMAKE_CXX_COMPILER=g++ -DCMAKE_CC_COMPILER=gcc
-- The C compiler identification is AppleClang 10.0.1.10010046
-- The CXX compiler identification is AppleClang 10.0.1.10010046
-- Check for working C compiler: /Library/Developer/CommandLineTools/usr/bin/cc
-- Check for working C compiler: /Library/Developer/CommandLineTools/usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/g++
-- Check for working CXX compiler: /usr/bin/g++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
CMake Warning:
  Manually-specified variables were not used by the project:

    CMAKE_CC_COMPILER

-- Build files have been written to: /Users/nkabiliravi/git/mycpptutorial/helloworld-cmake/build
```

and then link them using *make* command into an executable file called *greet*.

```
$ make
Scanning dependencies of target greet
[ 33%] Building CXX object CMakeFiles/greet.dir/hello.cpp.o
[ 66%] Building CXX object CMakeFiles/greet.dir/main.cpp.o
[100%] Linking CXX executable greet
[100%] Built target greet
```

## Running the app

Run *greet* command like this:

```
$ ./greet
Hello World!
```
