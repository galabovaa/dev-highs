# Development and testing

### Motivation

Need to be able to track bugs more easily and have reliable information about
performance.

Compile time has increased, the size of the project as well as the complexity of
calls to internal data structures and the linking between them.

The state of some of the interfaces and platform builds is unclear or untested.

See motivation-guidelines-testing.

### Suggested improvement

"scaffolding concept"

* maintain the conceptual integrity of the HiGHS code structure
* run test and development code without modifying current HiGHS repo source
* make sure behaviour corresponds to requirements and the documentaion is

  consistent and reflects that

### Suggested improvement implementation

Scaffold code at
https://www.github.com/galabovaa/scaffold.git

##### Pre-release unit tests

The Catch unit test library uses system-dependent code so we are removing the unit tests from master and moving them to bscaffold instead.
check/ becomes check-pre-release.

Leave a few feasible instances, one infeasible instance and one call with empty file.

##### Platforms

Windows, Linux and Mac are tested with GitHub Actions.

(todo:) Clang and GNU on Linux.

CMake Debug and Release.

##### Code Coverage

To build coverage info
after folder check/ (and other check-/ subdirs are copied)

``` bash
cmake -DCMAKE_BUILD_TYPE=DEBUG -DCI=ON -DHIGHS_COVERAGE=ON ..
make -j4
make ci_cov
```

##### Performance

##### Dev

