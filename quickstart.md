For those in a rush, here's how to get scrub working.
Download the latest tarball from the main google code page and do the following to build scrub:

```
$ tar xjf scrub-2.4.tar.bz2
$ cd scrub-2.4
$ ./configure
checking build system type... x86_64-unknown-linux-gnu
checking host system type... x86_64-unknown-linux-gnu
checking target system type... x86_64-unknown-linux-gnu
checking metadata... yes
checking installation directory variables... yes
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for gawk... gawk
checking whether make sets $(MAKE)... yes
checking whether to enable maintainer-specific portions of Makefiles... no
checking for gcc... gcc
checking for C compiler default output file name... a.out
checking whether the C compiler works... yes
checking whether we are cross compiling... no
checking for suffix of executables... 
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ANSI C... none needed
checking for style of include used by make... GNU
checking dependency style of gcc... gcc3
checking how to run the C preprocessor... gcc -E
checking for egrep... grep -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking getopt.h usability... yes
checking getopt.h presence... yes
checking for getopt.h... yes
checking whether byte ordering is bigendian... no
checking for an ANSI C-conforming const... yes
checking for getopt_long... yes
checking for special C compiler options needed for large files... no
checking for _FILE_OFFSET_BITS value needed for large files... no
checking for _LARGE_FILES value needed for large files... no
configure: creating ./config.status
config.status: creating Makefile
config.status: creating src/Makefile
config.status: creating man/Makefile
config.status: creating man/scrub.1
config.status: creating test/Makefile
config.status: creating config/config.h
config.status: executing depfiles commands
$ make
Making all in src
make[1]: Entering directory `/home/garlick/work/diskscrub/scrub-2.4/src'
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT aes.o -MD -MP -MF ".deps/aes.Tpo" -c -o aes.o aes.c; \
        then mv -f ".deps/aes.Tpo" ".deps/aes.Po"; else rm -f ".deps/aes.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT filldentry.o -MD -MP -MF ".deps/filldentry.Tpo" -c -o filldentry.o filldentry.c; \
        then mv -f ".deps/filldentry.Tpo" ".deps/filldentry.Po"; else rm -f ".deps/filldentry.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT fillfile.o -MD -MP -MF ".deps/fillfile.Tpo" -c -o fillfile.o fillfile.c; \
        then mv -f ".deps/fillfile.Tpo" ".deps/fillfile.Po"; else rm -f ".deps/fillfile.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT genrand.o -MD -MP -MF ".deps/genrand.Tpo" -c -o genrand.o genrand.c; \
        then mv -f ".deps/genrand.Tpo" ".deps/genrand.Po"; else rm -f ".deps/genrand.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT getsize.o -MD -MP -MF ".deps/getsize.Tpo" -c -o getsize.o getsize.c; \
        then mv -f ".deps/getsize.Tpo" ".deps/getsize.Po"; else rm -f ".deps/getsize.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT pattern.o -MD -MP -MF ".deps/pattern.Tpo" -c -o pattern.o pattern.c; \
        then mv -f ".deps/pattern.Tpo" ".deps/pattern.Po"; else rm -f ".deps/pattern.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT progress.o -MD -MP -MF ".deps/progress.Tpo" -c -o progress.o progress.c; \
        then mv -f ".deps/progress.Tpo" ".deps/progress.Po"; else rm -f ".deps/progress.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT scrub.o -MD -MP -MF ".deps/scrub.Tpo" -c -o scrub.o scrub.c; \
        then mv -f ".deps/scrub.Tpo" ".deps/scrub.Po"; else rm -f ".deps/scrub.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT sig.o -MD -MP -MF ".deps/sig.Tpo" -c -o sig.o sig.c; \
        then mv -f ".deps/sig.Tpo" ".deps/sig.Po"; else rm -f ".deps/sig.Tpo"; exit 1; fi
if gcc -DHAVE_CONFIG_H -I. -I. -I../config     -g -O2 -MT util.o -MD -MP -MF ".deps/util.Tpo" -c -o util.o util.c; \
        then mv -f ".deps/util.Tpo" ".deps/util.Po"; else rm -f ".deps/util.Tpo"; exit 1; fi
gcc  -g -O2   -o scrub  aes.o filldentry.o fillfile.o genrand.o getsize.o pattern.o progress.o scrub.o sig.o util.o  
make[1]: Leaving directory `/home/garlick/work/diskscrub/scrub-2.4/src'
Making all in man
make[1]: Entering directory `/home/garlick/work/diskscrub/scrub-2.4/man'
make[1]: Nothing to be done for `all'.
make[1]: Leaving directory `/home/garlick/work/diskscrub/scrub-2.4/man'
Making all in test
make[1]: Entering directory `/home/garlick/work/diskscrub/scrub-2.4/test'
make[1]: Nothing to be done for `all'.
make[1]: Leaving directory `/home/garlick/work/diskscrub/scrub-2.4/test'
make[1]: Entering directory `/home/garlick/work/diskscrub/scrub-2.4'
make[1]: Nothing to be done for `all-am'.
make[1]: Leaving directory `/home/garlick/work/diskscrub/scrub-2.4'
```

To scrub the second partition on Linux disk /dev/sda using default NNSA
algorithm, do the following.  Note that for normal SATA disks this will
take some time.

```
$ src/scrub /dev/sda2
scrub: using NNSA NAP-14.1-C patterns
scrub: please verify that device size below is correct!
scrub: scrubbing /dev/sda2 6234762240 bytes (~5GB)
scrub: random  |................................................|
scrub: random  |................................................|
scrub: 0x00    |................................................|
scrub: verify  |................................................|
$
```