# Pipes

## Intro
==========

Google Chrome is a wonderful browser in that if a tab of Google Chrome crashes only that single tab is 
killed. The rest of your tabs will continue to function normally. That really helps out when the whole
software doesn't crash. What Google Chrome uses is called Inter-Process communication(IPC), fancy talk for
“processes that can talk to each other.” This makes crashes in your program isolated, so it still fucntions 
normally. 

## What are pipes?
====================

Well Mario has pipes...

![Image of Mario Pipes](https://raw.githubusercontent.com/TheNerdJedi/Pipes/master/mario-pipes.png)

That's true, but the pipes that you use in IPC are known as **named pipes**

So unlike Mario's pipes, instead of pushing Mario through the pipes, you push data through the pipe.

## What can be moved in my pipes?
===================================

Just Mario pics...

Just joking, you can transfer all sorts of data between your processes but honestly *it depends*.
The rule of :thumbsup: is **KISS KISS**, *keep it short, stupid; keep it simple,stupid*. 
((BTW you are not stupid, the computer is.))

The type of data that is often transfered is usually:
- Command Codes: Check for update, download update, extract update, and install update (or cancel)
- Responses: If update available, if any changes in update, progress of current step(e.g. downloading)

With this the update happens separately than the program, isolating all crashes.

## I wanna play!
==================

Included is the C# source code for named pipes.
There are two files that do all the work(carry ftw): **PipeServer.cs** and **PipeClient.cs**
Along with that is a simple messaging program to demo communication.
Just click **Run** for each one! (Make sure you have Microsoft Visual Studio or something similar)

![Demo](https://raw.githubusercontent.com/TheNerdJedi/Pipes/master/server-client.png)
      

Influenced by:
[wyDay](http://wyday.com/blog/2010/multi-process-c-sharp-application-like-google-chrome-using-named-pipes/)