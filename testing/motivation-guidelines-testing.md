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
