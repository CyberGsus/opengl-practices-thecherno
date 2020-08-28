# opengl-practices-thecherno

This repository tracks all the code I will include when following [TheCherno](https://www.youtube.com/user/TheChernoProject) on Youtube!

## Building

This project uses [`cmake`](https://cmake.org) to configure and build. Targets are Linux only, as far as I'm concerned.

- Dependencies: `ninja` `g++`

```bash
/usr/bin/cmake --no-warn-unused-cli -DCMAKE_EXPORT_COMPILE_COMMANDS:BOOL=TRUE -DCMAKE_BUILD_TYPE:STRING=Debug -DCMAKE_C_COMPILER:FILEPATH=/bin/gcc -DCMAKE_CXX_COMPILER:FILEPATH=/bin/g++ -H/home/cyber/Downloads/test -B./build -G <your preferred building syste> -Werror -Wdeprecated
```
