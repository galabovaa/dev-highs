
# Development and testing

### Motivation

Need to be able to track bugs more easily and have reliable information about
performance.

Why using printing statements to debug isn’t great:

While adding debug statements to programs for diagnostic purposes is a common 
rudimentary technique, and a functional one (especially when a debugger is not
 available for some reason), it’s not that great for a number of reasons:

Debug statements clutter your code.
Debug statements clutter the output of your program.
Debug statements must be removed after you’re done with them, which makes them
non-reusable.
Debug statements require modification of your code to both add and to remove,
which can introduce new bugs.

Preprocessor macros are much safer but clutter the code even more.

CQSE Blog
Living in the #ifdef Hell: https://www.cqse.eu/en/blog/living-in-the-ifdef-hell/

It would be good to know that you won't affect highs execution with changes in
highs dev - it is for experimental code and analysis.


Compile time has increased, the size of the project as well as the complexity of
calls to internal data structures and the linking between them.

### Suggested improvement

"scaffolding concept"

- maintain the conceptual integrity of the HiGHS code structure
- run test and development code without modifying current HiGHS repo source
- make sure behaviour corresponds to requirements and the documentaion is
  consistent and reflects that

### Suggested improvement implementation

Scaffold code at
https://www.github.com/galabovaa/bscaffold.git

##### Pre-release unit tests
##### Platforms
##### Code Coverage
##### Performance
##### Dev