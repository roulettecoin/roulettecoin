Roulettecoin integration/staging tree
=====================================

http://www.roulettecoin.cc

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2014 Roulettecoin Developers

What is Roulettecoin?
---------------------

Roulettecoin is a lite version of Bitcoin using custom randomized proof-of-work algorithm that favours CPU mining.
 - 50 coins per block
 - 1 minute block targets
 - 1440 blocks (~1 day) to retarget difficulty
 - subsidy halves in 525.6k blocks (~1 year)
 - ~52.56 million total coins to be mined

For more information, as well as an immediately useable, binary version of
the Roulettecoin client sofware, see http://www.roulettecoin.cc.

License
-------

Roulettecoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/roulettecoin/roulettecoin/tags) are created
regularly to indicate new official, stable release versions of Roulettecoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test roulettecoin-qt.pro
    make -f Makefile.test
    ./roulettecoin-qt_test

