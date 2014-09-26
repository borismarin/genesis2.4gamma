GENESIS Version 2.4
===================

This is a stripped-down version of the [``official'' GENESIS 2.4
distribution](https://github.com/borismarin/genesis2.4gamma). 

Most of the (legacy) architecture-dependant Makefiles have been
removed, in order to use an unified autoconf-generated Makefile which
has been verified to work for both modern (circa 2014) Linux and OSX
(see notes below).


Building and Installing GENESIS
-------------------------------

For Linux, OSX (see notes below) and potentially BSD, it should be
sufficient to 

    $ ./configure
    $ make



### Mac OSX notes

- The current version has been verified to compile correctly only with
_gcc_ on OSX (where default compiler is _clang_). It can be installed
via 
        brew install https://raw.github.com/Homebrew/homebrew-versions/gcc48.rb

- You will need X11 in order to compile Xodus (otherwise,
you can always ```make nxgenesis```). You can get it from
[XQuartz](http://xquartz.macosforge.org/landing/).

- _Flex_ and _Bison_ are required, and can be installed via
        brew install flex bison
   




