# Guidelines for HiGHS interfaces design 

API vs SDK

It should be no surprise then that, when an SDK is used to create an application that has to communicate to other applications, it includes an API for this functionality. Inversely, an API is used for communication, but cannot be used solely to create a brand new application.

Another way to understand this is to think in terms of houses. APIs are telephone lines, allowing for communication in and out of the house. The SDK is the house itself and all of its contents.


### Good API design
https://www.toptal.com/api-developers/5-golden-rules-for-designing-a-great-web-api

Make sure people can actually use your API and that it works the first time, every time. Have new people try to implement your API occasionally to verify that it’s not confusing in some way that you’ve become immune to.

Keep it simple. Don’t do any fancy authentication. Don’t do some crazy custom URL scheme. Don’t reinvent SOAP, or JSON, or REST, or anything. Use all the tools you can that have already been implemented and are widely accepted, so that developers only have to learn your API, not your API + 10 obscure new technologies.

Provide language-specific libraries to interface with your service. There are some nice tools to automatically generate a library for you, such as Alpaca or Apache Thrift. Currently Alpaca supports Node, PHP, Python, and Ruby. Thrift supports C++, Java, Python, PHP, Ruby, Erlang, Perl, Haskell, C#, Cocoa, JavaScript, Node.js, Smalltalk, OCaml, Delphi and more.

Simplify any necessary signup. If you are not developing an open source API, or if there is a signup process of any sort, make sure that upon signup, a user is very quickly directed to a tutorial. And make the signup process completely automated without any need for human interaction on your part.

Provide excellent support. A big barrier to adoption is lack of support. How will you handle and respond to a bug report? What about unclear documentation? An unsophisticated user? Forums, bug trackers, and email support are fantastic starts, but do m