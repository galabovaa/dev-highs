# HiGHS Release 1.0

The transformation of a program into a maintaiable user product can be defined by the following components:
* Program
* Product
  * Generalization
  * Documentation
  * Testing
* System
  * Build
  * Platforms
  * Linking
  * Interfaces
* Programming System Product

### Program
HiGHS code

### Product
Generalization
  solvers: Mip, Ipx
  problem types: mip, qp
Documentation
  docsy
Testing
  code coverage
  unit tests
  extended cmake tests

### System
Windows and MacOS

SCIP interface
OSI interface

Language interfaces

CMake
* build
  * install ctest instances subset
* install HiGHS
* export targets for other CMake projects

### Programming System Product

HiGHS

Resources
* website [highs.dev]
* github repo | master | latest version | tests passing
* documentation site (highs-docsy) about.md = README.md

Targets
* executable
* shared library (optional static)
* interfaces