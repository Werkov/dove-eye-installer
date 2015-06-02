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

## Note on libglviewer

In official Debian (jessie) and Ubuntu (>= trusty) repositories there is
package `libqglviewer` which provides the necessary component for `dove-eve`.
However, the package is built for Qt4 and `dove-eye` is using Qt5 making it
incompatible to use together. Fortunately, latest Debian (experimental) already
provides prototype of the [package][1] built for Qt5. I forked the package (at
`0fc3249`), renamed it to `libqglviewer-qt5-dev` to prevent name clashes with
original package and [published it on Launchpad][2].

Later (in few months (as of 2015-06-02)), the official build for Qt5 should be
available.

[1]: https://packages.debian.org/experimental/libqglviewer-dev
[2]: https://launchpad.net/~werkov/+archive/ubuntu/ppa


