Nick Davis, 9-24-11

Building statically on Mac OS X isn't supported (or even possible) out of the 
box).  The error when using -static in gcc compilation is:

ld: library not found for -lcrt0.o

This code builds a crt0.o object file.

I discovered the code in a roundabout way.  The code was linked in an Apple 
discussion thread based on a suggested (but strongly discouraged) workaround on 
enabling static builds.  The Apple suggestion is apparently from 2002, so it may
not work on modern systems.  I tried on Mac OS X Lion and received errors, so 
didn't pursue it further, opting for an alternative with dynamic linking.

The thread URL:  https://discussions.apple.com/thread/2252567?threadID=2252567&tstart=-1

Source code URL http://www.opensource.apple.com/source/Csu/Csu-79/

The code is licensed under the Apple Public Source License.
