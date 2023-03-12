# libelf
FreeBSD's libelf implementation ported to GNU Make, extracted from elftoolchain

## Why?
The traditional Linux libelf implementation, which is provided by elfutils, has numerous problems building on musl-based systems. Furthermore, the implementation provided by FreeBSD is substantially lighter.

## Building
This implementation of libelf depends on libbsd at build time.

Building is a simple matter of running `make` in the source directory. There is no install rule in the makefile, but manpages and the resultant libelf.so can be easily copied into your location of choice.
