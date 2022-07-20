# Rules for Effective Source Code Control

Most developers have at least tried using a source code control system at one time or another. If you’re working on a development project as part of a team, such a system is practically indispensible as a way to prevent team members from tripping on each other’s changes. Even if you’re working all by yourself, source code control can provide a valuable safety net, saving a separate copy of your code in a secure repository and providing you a way to undo major mistakes.

But just how effective is your source code control? Like other parts of the development world, there are ways to make source code control work harder on your behalf. In this article, I’ll give you some tips on getting the most out of your source code control system.

 ### Rule #1: Choose the Right System
There are many source code control systems on the market. Rather than just picking the one you know about, or the one that comes for free with your IDE, it’s worth taking the time to seriously evaluate the alternatives. You’ll probably find some that fit in better with your development style than others. Here are a few factors to consider:

Price – Some systems are free. Others will cost you hundreds of dollars per user (or even more).
Concurrent development style – Some systems require you to actively check out code before working on it. Others let you change anything you like, and then merge the changes when you’re ready to commit them.
Repository – Does the system store data in a database, or in the file system? Are you comfortable with the safety and security of the repository?
Internet friendliness – If your team is geographically distributed, make sure that the system you choose works well over TCP/IP, without using up excessive bandwidth.
IDE integration – Some people really care whether the can perform source code control operations from within their IDE. Others don’t.
Cross-platform support – If you need to do development on more than one platform (say, Windows and Linux), you’ll want a system that works on both platforms.
There are lots of different systems out there to choose from. Without looking into the enterprise market, here are a few you might like to consider (listed in alphabetical order so as not to play favorites):

 ### Rule #2: Put the Right Things in the System
Smart teams use the source code control repository for more than just source code. The key is to store any artifact that’s not easily rebuilt from other artifacts. I use “Artifact” as a general term for anything having to do with your software product. Here are a few things you might consider storing in your source code control system:

Source code
Windows Installer databases
Database build scripts
Icons, bitmaps, and other graphics
License files
Readme files
Informal development notes
Documentation
Help files
Build scripts
Test scripts
Having everything in one place makes life much simpler when you’re faced with the inevitable support request for an older version of your product. You can take a clean machine, get a copy of everything that was involved in version 2.15, rebuild and you’re off. This is much easier than trying to collect source code from one place, database scripts from another, and bitmaps from a third – if anyone even bothered to save old database scripts.

Remember, too, that once you store something in the system, you must manage it through the system. Don’t let developers (or anyone else) copy things off to a private sandbox with the intent of checking them in later. Once a file escapes from source code control, you’ll lose the ability to easily re-create the state of your project at a point in time.

### Rule #3: Don’t Hog the Files
The best developers make frequent small changes to the repository, rather than a few huge changes. In a check-in/edit/check-out system (like Visual SourceSafe) this means only checking out a few files at a time. In an edit/merge/continue system (like CVS) this means committing changes after each task, rather than waiting until the end of a day or even longer.

Minimizing the size of changes has several good effects. First, if you are working with a system that locks files, you can avoid locking other people out for longer than necessary. Second, by keeping your commits small, you vastly lower the chance of needing to merge two incompatible versions of code. Finally, by working in small chunks, you can keep the comments in the source code control system targeted and informative.

And of course, you should strive to have an informative check-in comment for every check-in. If you can’t think of a way to summarize your changes, why did you even make them?

### Rule #4: Use Labels and Branches Wisely
Labels (sometimes called tags) give you a way to mark a versioned set of files with some friendly name. This is useful because humans are much better at remembering things like “Beta 2” than “Version 3019.4”. You should apply a label to your source code control repository at any significant point in time. This includes:

Public releases of the software
The start and finish of major code changes
The incorporation of a new third-party component
Builds that pass basic QA testing
Effective use of labels makes it easy to jump back to a particular point in time, whether to undo a terrible mistake or to see what state the system was in at that time.

By contrast, branches give you a way to develop two sets of source code for the same project in parallel. You should create a branch whenever different developers in the same project are following different rules. For example, if one team is finishing up version 1, while another is starting on version 2, that’s a good time for a branch. Presumably the first group of developers is checking in small, careful changes, while the other is roughing out the broad outlines of new features. Because the rules for these activities are different, they can’t easily be performed in a single set of source code files.

Branching is useful for exploration as well. If your main line of code is using a known, stable technique, but you want to explore a faster and potentially unstable way of accomplishing the same objectives, you should create a branch to explore the consequences. If the branch works out well, merge its changes back to the main line. If not, just stop working in the branch.

Finally, don’t create a branch just because you know you’ll need it in the future. Wait to make the version 2.0 branch until someone is actually going to work on it, to avoid extra merging before it’s really needed.

A Word to the Wise
Source code control is one of those basic practices that every developer should use on every project. With the availability of several excellent free systems, there’s no excuse for working without the source code control safety net. After you get used to storing files in a source code control repository, take the time to learn what else your system can do for you. You might just be surprised at the difference that it makes to your development efforts.

Mike Gunderloy is the author of over 20 books and numerous articles on development topics, and the lead developer for Larkware. Check out his new Sybex book Coder to Developer, which includes more advice on source code control and a wealth of other topicsx. When he’s not writing code, Mike putters in the garden on his farm in eastern Washington state.



