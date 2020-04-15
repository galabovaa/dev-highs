HiGHS Testing
-------------

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

HiGHS
-----
git ergo:
code reviews (brief)
actions:
to ensure consistency, readability and to avoid unnecessary merge conflicts
 - lint

Initial suggested test environment structure:

"Scaffold" (on git, separately)
 - callback testing env:
   - file outside highs
   - implements "dumpHMO()"

     - use within HiGHSDEV

testing/debugging (J)
 - TESTS_FOLDER
 - TestHmo.cpp => builds exe which J's

Testing

Testing i-cpp
learning, HiGHS context

cpp general checkers

    clang-format-lint
      github action on
    cppcheck:
      4 errors test basis solve
      2 errors ipx
      3 errors filereader
    valgrind
      .
    clang-tidy:
    cppclean: lots of warnings
    cpplint woohoo

github actions
  can be script (like ctest but outside of HiGHS)