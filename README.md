  __  __   __   __  __          
 |  \/  | /_ | |  \/  |         
 | \  / |  | | | \  / |  ______ 
 | |\/| |  | | | |\/| | |______|
 | |  | |  | | | |  | |         
 |_|  |_|  |_| |_|  |_|         

  __  __               _           _                    ____            _                    _   
 |  \/  |             | |         | |                  |  _ \          | |                  | |  
 | \  / |   ___     __| |  _   _  | |   __ _   _ __    | |_) |   ___   | |_   _ __     ___  | |_ 
 | |\/| |  / _ \   / _` | | | | | | |  / _` | | '__|   |  _ <   / _ \  | __| | '_ \   / _ \ | __|
 | |  | | | (_) | | (_| | | |_| | | | | (_| | | |      | |_) | | (_) | | |_  | | | | |  __/ | |_ 
 |_|  |_|  \___/   \__,_|  \__,_| |_|  \__,_| |_|      |____/   \___/   \__| |_| |_|  \___|  \__|
                                                                                                 

Concept:

The idea is to build some modular malware with the goal of creating a botnet. This is a strictly
in-the-lab effort for educational reasons, of course. As we're shooting for a group project and
modular architecture, those of you who are trying to learn programming and/or C++ can still have
a valuable role to play.


Target:

We're targeting Windows (big surprise) and might as well keep it all there. The project files
will all be based around MS Visual C++. You can grab Visual C++ 2010 Express for free at the URL:
https://www.microsoft.com/visualstudio/en-us/products/2010-editions/visual-cpp-express


Features for version 0.1:

 - Completely modular
 - Core and modules/plugins for actual functionality.
 - Module types: Foothold/Install, C&C Client, Payload


Initial Modules:

- Foothold/Install: Basic Windows Service - We'll just install ourselves as a Windows service
  upon execution. It easy and simple, and if the thing blows up we can just sc delete it.
 - C&C Client: Basic Sockets / Plaintext - No encryption or coolness. We just run it all telnet
  style. We also need to build  server and create a protocol.
 - Payload: Bragging / Uninstall - Upon pwnership of a new boxen, we'll let the use know and 
  give them a nice uninstall button. Just in case we blow some stuff up...


ProTips:

[1] Protip: C++ doesn't really have "interfaces"[2] the way Java has interfaces. Instead we 
  have parent classes with virtual functions.
[2] Protip: [3] An interface essentially abstracts out an object so we can make assumptions
  about it so we can use it even if we don't know exactly what it is. Think of yourself as an
  object (sorry ladies!) and "person" as the interface. We know generally what a person is and
  how we can interact with it, but we don't know every person explicitly. We can treat them 
  basically the same and we'll be fine.
[3] Protip: Yo dawg, I heard you like protips.


Current Delegated Tasks:

-Chris_Bad2Beef- I'm going to build out the core and need to create interfaces[1] for us all
  to base code around.
-Seb- I'd like to work on some of the client/server socket stuff layered in TLS once its 
  working without encryption, mostly because I want some experience building an app with 
  that functionality.
-Morfir- I will be working on managing the git repo, as well as other things I will find out
  tonight. Also for all of you using linux, I will be working on a way to do cross-compiling
  for the C++ code. For now however we will be booting VM's with Windows on it for a common OS.
-Everyone Else- In the mean time we should all be helping each other out getting bootstrapped
  with C++. The link to the IDE is above. Everyone should try the basic C++ hello world and 
  we can start building from there. You can definitely ask questions.