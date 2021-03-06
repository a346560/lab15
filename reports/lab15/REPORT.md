## Laboratory work XV

Данная лабораторная работа посвещена изучению инструментов статического анализа кода на примере **cppcheck**

```ShellSession
$ open http://cppcheck.sourceforge.net
```

## Tasks

- [V] 1. Ознакомиться со ссылками учебного материала
- [V] 2. Используя **cppcheck** провести анализ проекта на **C++**
- [V] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Links

- [Cppcheck](http://cppcheck.sourceforge.net/manual.pdf)

## Tutorial

```ShellSession
$ export GITHUB_USERNAME=a346560
$ git clone https://github.com/${GITHUB_USERNAME}/lab04-1 lab15
$ cd lab15
$ git remote remove origin
$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab15
$ cmake -H. -B_build
$ cmake --build _build
$ cmake --build _build
$ cmake --build _build --target print
$ cmake --build _build --target example1
$ cmake --build _build --target example2
$ cmake -DCMAKE_EXPORT_COMPILE_COMMANDS=ON .
cppcheck ~/vershinin/lab15
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: SDCC...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: SIMULATE_VERSION_PATCH...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: SIMULATE_VERSION_PATCH;SIMULATE_VERSION_TWEAK...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _CRAYC...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_BUILD;_MSC_VER...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_FULL_VER;_MSC_VER...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_VER...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_VER;_WIN32...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_VER;__clang__...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _M_I86;__WATCOMC__...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _M_IX86;__WATCOMC__...
1/11 files checked 9% done
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: SIMULATE_VERSION_PATCH...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: SIMULATE_VERSION_PATCH;SIMULATE_VERSION_TWEAK...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _CRAYC...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_BUILD;_MSC_VER...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_FULL_VER;_MSC_VER...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_VER...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_VER;_WIN32...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_VER;__clang__...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _M_I86;__WATCOMC__...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _M_IX86;__WATCOMC__...
Checking /home/user/vershinin/lab15/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: __APPLE__...
2/11 files checked 18% done
Checking /home/user/vershinin/lab15/CMakeFiles/feature_tests.c...
3/11 files checked 27% done
Checking /home/user/vershinin/lab15/CMakeFiles/feature_tests.cxx...
4/11 files checked 36% done
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: SDCC...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: SIMULATE_VERSION_PATCH...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: SIMULATE_VERSION_PATCH;SIMULATE_VERSION_TWEAK...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _CRAYC...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_BUILD;_MSC_VER...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_FULL_VER;_MSC_VER...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_VER...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_VER;_WIN32...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _MSC_VER;__clang__...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _M_I86;__WATCOMC__...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdC/CMakeCCompilerId.c: _M_IX86;__WATCOMC__...
5/11 files checked 45% done
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: SIMULATE_VERSION_PATCH...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: SIMULATE_VERSION_PATCH;SIMULATE_VERSION_TWEAK...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _CRAYC...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_BUILD;_MSC_VER...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_FULL_VER;_MSC_VER...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_VER...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_VER;_WIN32...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _MSC_VER;__clang__...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _M_I86;__WATCOMC__...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: _M_IX86;__WATCOMC__...
Checking /home/user/vershinin/lab15/_build/CMakeFiles/3.5.1/CompilerIdCXX/CMakeCXXCompilerId.cpp: __APPLE__...
6/11 files checked 54% done
Checking /home/user/vershinin/lab15/_build/CMakeFiles/feature_tests.c...
7/11 files checked 63% done
Checking /home/user/vershinin/lab15/_build/CMakeFiles/feature_tests.cxx...
8/11 files checked 72% done
Checking /home/user/vershinin/lab15/examples/example1.cpp...
9/11 files checked 81% done
Checking /home/user/vershinin/lab15/examples/example2.cpp...
10/11 files checked 90% done
Checking /home/user/vershinin/lab15/sources/print.cpp...
11/11 files checked 100% done
(information) Too many #ifdef configurations - cppcheck only checks 12 configurations. Use --force to check all configurations. For more details, use --enable=information.


```
Copyright (c) 2017 Братья Вершинины
```
