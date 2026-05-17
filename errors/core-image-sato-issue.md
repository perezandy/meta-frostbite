I got this error after running core image sato:

```
bitbake core-image-sato
```

```
WARNING: Host distribution "cachyos" has not been validated with this version of the build system; you may possibly experience unexpected failures. It is recommended that you use a tested distribution.
Loading cache: 100% |############################################################################################| Time: 0:00:00
Loaded 1940 entries from dependency cache.
NOTE: Resolving any missing task queue dependencies

Build Configuration:
BB_VERSION           = "2.16.0"
BUILD_SYS            = "x86_64-linux"
NATIVELSBSTRING      = "cachyos"
TARGET_SYS           = "x86_64-poky-linux"
MACHINE              = "qemux86-64"
DISTRO               = "poky"
DISTRO_VERSION       = "5.3.3"
TUNE_FEATURES        = "m64 x86-64-v3"
TARGET_FPU           = ""
meta                 = "HEAD:ab57471acad7ce2a037480dc7b301104620f1ebf"
meta-poky            
                     = "HEAD:9b98ec5e6cfb6c9dc74d3c2e6304eeb274f7c487"

WARNING: Your host glibc version (2.43) is newer than that in uninative (2.42). Disabling uninative so that sstate is not corrupted.
Sstate summary: Wanted 3794 Local 0 Mirrors 0 Missed 3794 Current 908 (0% match, 19% complete)##########         | ETA:  0:00:00
Initialising tasks: 100% |#######################################################################################| Time: 0:00:01
NOTE: Executing Tasks
ERROR: m4-native-1.4.20-r0 do_compile: oe_runmake failed
ERROR: m4-native-1.4.20-r0 do_compile: Execution of '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/run.do_compile.37415' failed with exit code 1
ERROR: Logfile of failure stored in: /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/log.do_compile.37415
Log data follows:
| DEBUG: Executing shell function do_compile
| NOTE: make -j 16 infodir=/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/share/info
| cd checks && make
| make[1]: Entering directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build/checks'
| make[1]: Nothing to be done for 'all'.
| make[1]: Leaving directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build/checks'
| make  all-recursive
| make[1]: Entering directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build'
| Making all in .
| make[2]: Entering directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build'
| make[2]: Nothing to be done for 'all-am'.
| make[2]: Leaving directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build'
| Making all in examples
| make[2]: Entering directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build/examples'
| make[2]: Nothing to be done for 'all'.
| make[2]: Leaving directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build/examples'
| Making all in lib
| make[2]: Entering directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build/lib'
| make  all-am
| make[3]: Entering directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build/lib'
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-asyncsafe-spin.o `test -f 'asyncsafe-spin.c' || echo '../../sources/m4-1.4.20/lib/'`asyncsafe-spin.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-openat-proc.o `test -f 'openat-proc.c' || echo '../../sources/m4-1.4.20/lib/'`openat-proc.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-gl_avltree_oset.o `test -f 'gl_avltree_oset.c' || echo '../../sources/m4-1.4.20/lib/'`gl_avltree_oset.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-basename-lgpl.o `test -f 'basename-lgpl.c' || echo '../../sources/m4-1.4.20/lib/'`basename-lgpl.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-btowc.o `test -f 'btowc.c' || echo '../../sources/m4-1.4.20/lib/'`btowc.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c-stack.o `test -f 'c-stack.c' || echo '../../sources/m4-1.4.20/lib/'`c-stack.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32isalnum.o `test -f 'c32isalnum.c' || echo '../../sources/m4-1.4.20/lib/'`c32isalnum.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32isalpha.o `test -f 'c32isalpha.c' || echo '../../sources/m4-1.4.20/lib/'`c32isalpha.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32isblank.o `test -f 'c32isblank.c' || echo '../../sources/m4-1.4.20/lib/'`c32isblank.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32iscntrl.o `test -f 'c32iscntrl.c' || echo '../../sources/m4-1.4.20/lib/'`c32iscntrl.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32isdigit.o `test -f 'c32isdigit.c' || echo '../../sources/m4-1.4.20/lib/'`c32isdigit.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32isgraph.o `test -f 'c32isgraph.c' || echo '../../sources/m4-1.4.20/lib/'`c32isgraph.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32islower.o `test -f 'c32islower.c' || echo '../../sources/m4-1.4.20/lib/'`c32islower.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32isprint.o `test -f 'c32isprint.c' || echo '../../sources/m4-1.4.20/lib/'`c32isprint.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32ispunct.o `test -f 'c32ispunct.c' || echo '../../sources/m4-1.4.20/lib/'`c32ispunct.c
| gcc   -I. -I../../sources/m4-1.4.20/lib   -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include  -Wno-cast-qual -Wno-conversion -Wno-float-equal -Wno-sign-compare -Wno-undef -Wno-unused-function -Wno-unused-parameter -Wno-float-conversion -Wimplicit-fallthrough -Wno-pedantic -Wno-sign-conversion -Wno-type-limits -Wno-unused-const-variable -Wno-unsuffixed-float-constants -Wno-error -isystem/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/recipe-sysroot-native/usr/include -O2 -pipe -std=gnu99 -c -o libm4_a-c32isspace.o `test -f 'c32isspace.c' || echo '../../sources/m4-1.4.20/lib/'`c32isspace.c
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/basename-lgpl.c:19:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/gl_avltree_oset.c:18:
| ./stdlib.h:827:20: error: expected identifier or '(' before '_Generic'
|   827 | _GL_EXTERN_C void *bsearch (const void *__key,
|       |                    ^~~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/openat-proc.c:20:
| ./stdlib.h:827:20: error: expected identifier or '(' before '_Generic'
|   827 | _GL_EXTERN_C void *bsearch (const void *__key,
|       |                    ^~~~~~~
| make[3]: *** [Makefile:4160: libm4_a-basename-lgpl.o] Error 1
| make[3]: *** Waiting for unfinished jobs....
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32ispunct.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32islower.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/btowc.c:18:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32isgraph.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32isalnum.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32isprint.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32isblank.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32isalpha.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32isspace.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32iscntrl.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c32isdigit.c:17:
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| ./wchar.h:838:23: error: expected identifier or '(' before '_Generic'
|   838 | _GL_EXTERN_C wchar_t *wmemchr (const wchar_t *__s, wchar_t __wc, size_t __n)
|       |                       ^~~~~~~
| make[3]: *** [Makefile:4146: libm4_a-gl_avltree_oset.o] Error 1
| make[3]: *** [Makefile:4300: libm4_a-c32iscntrl.o] Error 1
| make[3]: *** [Makefile:4258: libm4_a-c32isalnum.o] Error 1
| make[3]: *** [Makefile:4384: libm4_a-c32isspace.o] Error 1
| make[3]: *** [Makefile:4328: libm4_a-c32isgraph.o] Error 1
| make[3]: *** [Makefile:4272: libm4_a-c32isalpha.o] Error 1
| make[3]: *** [Makefile:4356: libm4_a-c32isprint.o] Error 1
| make[3]: *** [Makefile:4286: libm4_a-c32isblank.o] Error 1
| make[3]: *** [Makefile:4342: libm4_a-c32islower.o] Error 1
| make[3]: *** [Makefile:4314: libm4_a-c32isdigit.o] Error 1
| make[3]: *** [Makefile:4370: libm4_a-c32ispunct.o] Error 1
| ./stdlib.h:827:20: error: expected identifier or '(' before '_Generic'
|   827 | _GL_EXTERN_C void *bsearch (const void *__key,
|       |                    ^~~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/asyncsafe-spin.c:19:
| ./stdlib.h:827:20: error: expected identifier or '(' before '_Generic'
|   827 | _GL_EXTERN_C void *bsearch (const void *__key,
|       |                    ^~~~~~~
| In file included from /usr/include/features.h:540,
|                  from /usr/include/assert.h:35,
|                  from ./config.h:4115,
|                  from ../../sources/m4-1.4.20/lib/c-stack.c:36:
| ./stdlib.h:827:20: error: expected identifier or '(' before '_Generic'
|   827 | _GL_EXTERN_C void *bsearch (const void *__key,
|       |                    ^~~~~~~
| make[3]: *** [Makefile:4202: libm4_a-btowc.o] Error 1
| make[3]: *** [Makefile:4118: libm4_a-asyncsafe-spin.o] Error 1
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| ./string.h:777:20: error: expected identifier or '(' before '_Generic'
|   777 | _GL_EXTERN_C void *memchr (const void *__s, int __c, size_t __n)
|       |                    ^~~~~~
| make[3]: *** [Makefile:4230: libm4_a-c-stack.o] Error 1
| make[3]: *** [Makefile:4132: libm4_a-openat-proc.o] Error 1
| make[3]: Leaving directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build/lib'
| make[2]: *** [Makefile:3608: all] Error 2
| make[2]: Leaving directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build/lib'
| make[1]: *** [Makefile:2530: all-recursive] Error 1
| make[1]: Leaving directory '/home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/build'
| make: *** [Makefile:2486: all] Error 2
| ERROR: oe_runmake failed
| WARNING: /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/run.do_compile.37415:182 exit 1 from 'exit 1'
| WARNING: Backtrace (BB generated script):
|  #1: bbfatal_log, /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/run.do_compile.37415, line 182
|  #2: die, /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/run.do_compile.37415, line 166
|  #3: oe_runmake, /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/run.do_compile.37415, line 161
|  #4: autotools_do_compile, /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/run.do_compile.37415, line 156
|  #5: do_compile, /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/run.do_compile.37415, line 151
|  #6: main, /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/run.do_compile.37415, line 195
ERROR: Task (/home/andy/frostbite/layers/openembedded-core/meta/recipes-devtools/m4/m4-native_1.4.20.bb:do_compile) failed with exit code '1'
NOTE: Tasks Summary: Attempted 525 tasks of which 524 didn't need to be rerun and 1 failed.

Summary: 1 task failed:
  /home/andy/frostbite/layers/openembedded-core/meta/recipes-devtools/m4/m4-native_1.4.20.bb:do_compile
    log: /home/andy/frostbite/build/tmp/work/x86_64-linux/m4-native/1.4.20/temp/log.do_compile.37415
Summary: There were 2 WARNING messages.
Summary: There were 2 ERROR messages, returning a non-zero exit code.
```
