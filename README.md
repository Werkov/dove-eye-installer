General
=======

Upon clone, initialize submodules.

    git submodule init
    git submodule update


Debian package
==============

Install build dependencies (list them) and build package

    dpkg-ckechbuilddeps || apt-get install ...
    dpkg-buildpackage

