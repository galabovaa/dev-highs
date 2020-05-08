# Interfaces Design Doc

# Motivation

HiGHS should be easy to use in a consistent, well documented way. 

Pre-release state:

Various progress in some of what is listed below.

# Interfaces

SCIP
OSI
GAMS
Julia
Fortran
Matlab
Mosek
AMPL
C#
R

###### LP Input File Supported Formats
- LP
- MPS
- EMS

## Suggestions 
Inconsistency in interfaces exposed in relation to Java 
Decision to have interfaces relying on external code in a separate repo in ERGO-Code

jump-dev/HiGHS.jl
uses C rather than C++ so will make another repo and aim to achieve MOI unit tests pass

For languages which can talk to C++ directly it makes sense to do that. 

C++ API should handle such cases. 
  - Consistent with Highs.h 
  - maybe a good way of sorting out top level spaghetti
  - HiGHS Component idea? more on API design see design-doc-interfaces 
  WIP, first get the Julia link to work

# Java
Recent interacions with someone intersted from Java. 

Java can call C++ but not so straight forward. S tried with JNI "not a straightforward task" but other options exist, some warn about bug introductio, others argue passionately.

Suggested FluentAPI design for calls to Java and maybe others? LP builder type of thing. Add to java interface first.



