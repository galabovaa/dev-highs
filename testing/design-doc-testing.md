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

- maintain the conceptual integrity of the HiGHS code structure
- run test and development code without modifying current HiGHS repo source
- make sure behaviour corresponds to requirements and the documentaion is

  consistent and reflects that

### Suggested improvement implementation

Scaffold code at
https://www.github.com/galabovaa/scaffold.git
See README.md and comments in the CMakeLists.txt in each subdir.

dev-presolve/ is an example of how one would use the scaffold for development. See the README in scaffold/ and the guide.md in dev-highs. It is an example of a folder which can exist locally or on any git branch of scaffold/ which can be copied into HiGHS for development or test of that component. The scaffold/ repo will contain scaffold utilities and will define the scaffold executable, which will run unit tests on HiGHS and some component tests if we want to link them. dev-presolve defines it's own executable

The scaffold defines an executable, however it is build with a header-only library structure in mind. Do not define cpp files: Instead use only headers and CMake INTERFACE targets to link against, if needed. This ensures no linking problems in the future and is the easiest if it is code which will only test a component (and that should be the intention when writing tests)

Targets are build with CMake. Some scaffold subdirs are meant to be included at the bottom of the HiGHS root CMakeLists.txt, some are not meant to be included, like the one currently defined in scaffold/unit_test/, which for the moment is its own project.

##### Pre-release unit tests

The Catch unit test library uses system-dependent code so we are removing the unit tests from master and moving them to scaffold instead.

Will leave a few feasible instances, one infeasible instance and one call with empty file.

##### Platforms

Windows, Linux and Mac are tested with GitHub Actions.

Clang is tested by Ivet on her new Mac :)

CMake Debug and Release.

##### Code Coverage

To build coverage info
todo: after unit tests are sorted, and maybe cmake-targets branch cleanup

```bash
cmake -DCMAKE_BUILD_TYPE=DEBUG -DCI=ON -DHIGHS_COVERAGE=ON ..
make -j4
make ci_cov
```

##### Performance

##### Dev

The repo dev-presolve is an example of how one would use utilities defined in HiGHS from outside of HiGHS//.
