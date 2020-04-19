General points to consider
--------------------------

Avoid memory leaks through use shared pointers to manage memory allocation and cleanup
Use the Resource Acquisition Is Initialization (RAII) idiom to manage resource cleanup - especially in the presence of exceptions
Avoid calling virtual functions in constructors
Employ minimalist coding techniques where possible - for example, declaring variables only when needed, scoping variables, and early-out design where possible.
Truly understand the exception handling in your code - both with regard to exceptions you throw, as well as ones thrown by classes you may be using indirectly. This is especially important in the presence of templates.
RAII, shared pointers and minimalist coding are of course not specific to C++, but they help avoid problems that do frequently crop up when developing in the language.

Some excellent books on this subject are:

Effective C++ - Scott Meyers
More Effective C++ - Scott Meyers
C++ Coding Standards - Sutter & Alexandrescu
C++ FAQs - Cline
Reading these books has helped me more than anything else to avoid the kind of pitfalls you are asking about.

-----------------------

When making changes to your code, make behavioral changes OR structural changes, and then retest for correctness. Making behavioral and structural changes at the same time tends to lead to more errors as well as errors that are harder to find.

-----------------------

Defensive programming is a practice whereby the programmer tries to anticipate all of the ways the software could be misused, either by end-users, or by other developers (including the programmer themselves) using the code. These misuses can often be detected and then mitigated (e.g.by asking a user who entered bad input to try again).



* namespaces: are a strategy to remove clutter but a better strategy is design
* build dynamic / static libraries

