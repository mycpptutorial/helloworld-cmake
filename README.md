# helloworld-cmake

This sample is showing you how you can use cmake and CMakeLists.txtfile to compile your c++ application.

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
