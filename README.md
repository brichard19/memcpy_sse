# memcpy_sse
memcpy() using SSE2 load/store instrinsics.

Compiled with VC++ for 32-bit it out-performs memcpy(). When compiled for 64-bit it performs the same as memcpy(), because this is how memcpy() is already implemented since all x86-64 chips support SSE.

On Linux it seems to be faster than memcpy() in both 32-bit and 64-bit.


32-bit Linux:
```
g++ memcpy_test.cpp -o memcpy_test -O2 -msse2
```

64-bit Linux:
```
g++ memcpy_test.cpp -o memcpy_test -O2
```