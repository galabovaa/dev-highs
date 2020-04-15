### Motivation

###### Windows build
Pre-release HiGHS failed to build on Windows.

###### Linking against HiGHS
Calling highs from cpp: build dir and install dir
Was only tested with install dir only on linux with gcc.

Calling highs from cmake:
 and from cmake: build dir, install dir, github repo. Current state of master only works with the install dir. for the other configurations header Highs.h can not be found.

### Suggested improvement
Improved CMake Build
More Modern CMake 3.15 or above

Use targets and rules which enforce safety and correct include dependencies.
Do not use include_directories() and cmake compiler flags.

only compile parallel code if OPENMP is available.

Single highs target (ipx object target?)

### Suggested improvement implementation
Windows build fixed

highs-docsy Linking against HiGHS part.