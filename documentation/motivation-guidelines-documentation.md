HiGHS project documentation.
---------------------------

Motivation 

https://www.reddit.com/r/cpp/comments/8lwmkb/which_tool_do_you_use_to_document_your_c_code/
·

The problem with "automated" tools such as Doxygen is that they produce the illusion of documentation rather than documentation itself. They basically just paraphrase the code - which should be readable in the first place.

Documentation should include:

Description of what the program/library is supposed to do. What is it expected to be used for.

What is the user API, how does one use the the program/library - including tutorials and examples.

High level description of implementation strategy

What are the design decisions

What is the rationale/motivation for these decisions

Documentation should not include:

Implementation details. These should be in code itself. If the code is not obvious, then either the code should be changed or comments added.

Reference to any private implementation details.

Documentation prepration should be seen as an aid to building a coherent design rather than some afterthought to try and fix something that has been made over complicated in the first place.

I have a talk about this at CPPCon 2017: https://www.youtube.com/watch?v=YxmdCxX9dMk


--------------------------
Here are some key points to writing good API reference documentation:

Document the contract, not the implementation.1
Explain fuzzy verbs. What does "find" mean, versus "get"? Set users' expectations.
Document restrictions on arguments or return values that aren't fully conveyed by the signature (like that an integer has to be positive, or in the range 1-100, etc).
Cover failure and not just success. Can arguments be invalid? Can your code behave in abnormal ways even if the inputs are valid? How do you signal errors or other problems?
Be thorough but not verbose. Don't repeat information that's clear from the signature.


code itself constitutes documentation - which is an extremely important note, especially when determining what documentation already exists. 

----------------------------
Nice example: 

https://www.sfml-dev.org/documentation/2.5.1/

----------------------------
Initial suggested structure about HiGHS docs:

Public
~ description of public functionality 
* Project Specification ~
* User Manual ~
  Examples ~
* Website: ~ Guide is a good starting point 
* README.md

Private
* Specification of testing and development tools ~~
  CMake / Bazel ~~
* Usage ~~
* Design decisions
  
Private HiGHS ~~~
can be used for code for dev features in bscaffold

----------------------------

Done 

~ Public: Docsy 
~~ Private: dev-tasks
~~~ .md in scaffold code repo