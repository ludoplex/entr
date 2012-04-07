Event Notify Test Runner
========================

**entr** - a utility that for running arbitrary commands when files change.
Uses [kqueue(2)][kqueue_2] to avoid polling. Reads a list of files provided on
STDIN and run the supplied command if any of them change.

Installation
------------

    make
    make test
    install entr $HOME/local/bin/

Usage
-----

Run make when a source file changes:

    ls *.[hc] | entr `which make`


To watch for changes in any Python file and run some tests:

    find . -name *.py | entr ./test.sh

Platforms
---------

Tested on OpenBSD 5.0

[kqueue_2]: http://www.openbsd.org/cgi-bin/man.cgi?query=kqueue&apropos=0&sektion=0&manpath=OpenBSD+Current&format=html