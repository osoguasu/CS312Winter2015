###CS 312 Help Session

#####Getting started with Visual Studio

There are a couple free versions: Visual Studio Community Edition and Visual Studio Express. Taken from Microsoft's blog, the differences are:

> Visual Studio Express Editions are *targeting specific platforms*:  
* Express for Web allows you to develop Web apps;  
* Express for Windows allows you to develop Windows apps; 
* Express for Windows Desktop allows you to develop desktop apps.  
* Visual Studio Community Edition, you can develop projects targeting cross-platforms. 

They can be found here: 
* [Visual Studio Express Flavors](http://www.visualstudio.com/en-US/products/visual-studio-express-vs)
* [Visual Studio Community Edition](http://www.visualstudio.com/products/visual-studio-community-vs) 

**NOTE: For this class, you are going to be coding in C#, so if you use Express, you need an edition that supports C#. Basically, that's going to be the Desktop version**

The other big, bad paid versions can be obtained through the CS department two business days after the add/drop deadline for free. See the Syllabus for more info and links.

#####Using C# ("C Sharp")

To paraphrase Dr. Martinez's class page [found here](http://axon.cs.byu.edu/~martinez/classes/312/Resources/csharp):

> C# is often compared with Java ...
Probably more important, though, is how C# is different. While there are many ways, I will go over a few that are more immediate:
* In Java, the convention is for objects to start uppercase and methods lowercase. In C#, methods start uppercase also (conventionally).
* Java's accessor paradigm is getX() and setX( X ). C# has [properties](http://msdn.microsoft.com/en-us/library/x9fsa0sw.aspx) which treat accessors more like fields than methods.

More help resources can be found on the syllabus page. If you have not read the syllabus, we highly recommend and encourage you to do so now, and use those resources.

In addition, there are several other ways to become familiar with C#:
* [Safari E-Books](https://it.byu.edu/byu/help.do?sysparm_document_key=kb_knowledge,f2a5fbe70a0a3c09007a347985c9a282) (some recommended ones are "Learning C#" and "C# in a Nutshell")
* [The library for physical books](lib.byu.edu)
* [YouTube tutorials](https://www.youtube.com/results?search_query=c%23)

#####Key Tools within Visual Studio

Good resource for learning about debugging in Visual Studio: [Debug your app](http://www.visualstudio.com/get-started/debug-your-app-vs)

Some highlights of this article are:

* Debugger is integrated into the IDE, usually the green arrow across the top that says "Start"
* Exceptions will be highlighted when thrown by the app
* Breakpoints can be set when a line of code is reach, and can also be set conditionally
* Use the Locals window to see local variables and their values
* The call stack window will show the state of the stack (who called who) when you pause the debugger or an exception is thrown
* You can set variables to be watched as you step through the program.

Not in the article, but also quite useful is the Immediate Window which can be used to type commands and see how the program responds in it's current state.

#####Practice Application

Build a simple app with a button and two text fields to convert temperatures from Fahrenheit to Celsius.

#####More Info

Always check the syllabus, project specs for help, try searching Google, then the Google Group for the class, and finally we are available through the TA Email, our office hours, and by appointment.

###Questions?
