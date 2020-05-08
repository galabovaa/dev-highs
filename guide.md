# Release Version 1.0

Release versions will be changed manually from the HiGHS/CMakeLists.txt for the moment.

This set of documents serves as internal specification complimenting the source code along with the highs-docsy for public documentation (see section Documentation below) for the official HiGHS 1.0 resease.

The structure of this design-doc collection is based on the HiGHS structure outlined in dev-highs/design-doc.md
See the design docs in the subfolders for further details.

### April 2020

###### Next:

- Finish highs-docsy when builds (More Modern CMake) and interfaces (Julia) are ready for release.

###### Change Log

08.05 

> Added GitHub actions to scaffold/ making sure it builds on its own and with component/test
> Added -DFAST_BUILD to CMake options of HiGHS, start of CMake update for build and interfaces
> API design
  > Julia should talk to C++ directly
  > For Java consider FluentAPI design suggested by Sergey
    void * methods in Java or C++ API


24.04 Scaffold 1.0

> Documentation
> highs-docsy is mostly ready at https://galabovaa.github.io/highs-docsy/ (to be moved to ERGO-Code repo for release)
> about.md corresponds to the repo README.md
> Testing
> catch-out
> The unit tests with Catch/ can now be moved to scaffold/ along with other testing and development utilities.
> scaffold project version 1.0 up on github
> System
> Build

    Windows build was fixed for parallel code too, check for OpenMP Version now happens in CMake.
    Targets install and link correctly.

> Interfaces

    Most of the system dependent bits of code are removed. The unit tests need to be removed too. WIP More Modern CMake.
