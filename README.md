Notes about OpenBSD porting (tips, tricks, codesnippets, etc.)

This is a collection of my (kmos@openbsd) notes about tips, tricks, and
code snippets I use while doing OpenBSD ports. They tend towards being
about Python ports and/or fixing ports for sparc64.

On sparc64 and ports:

sparc64 has 2 major differences:

1. sparc64 is the last (as of 7.7-beta) architecture using the GCC in base
still supported by the ports tree[^1]. The GCC in base is 4.2.1 with lots of
local OpenBSD changes. The last version still GCC 2.x licensed. All the other
package-building architectures are using clang/LLVM. 

2. stuff about strict alignment

Also big endian, but powerpc (ew) is strict alignment

[^1]: Some other architectures that do not have official packages are
semi-supported by the ports tree. However, that is best effort and as
long as such support isn't a large burden upon the architectures that
still have official packages built for them.
