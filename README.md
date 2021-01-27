# OpenVec [![Travis Build Status](https://travis-ci.com/OpenVec/OpenVec.svg?branch=master)](https://travis-ci.com/OpenVec/OpenVec)
OpenVec enables portable explicit vectorization on different architectures

Just include `openvec.h` file in your C/C++ code and you are ready to go.

To compile code examples:
`make arch={intel64,knc,gccavx,neon}`

If no arch is provided, gcc with SSE will be used.

To run a self tests:
`make arch={intel64,knc,gccavx,neon} run_selftest`

The stencil* samples will allocate 3.9GB,
if you want allocate less memory edit `stencil_common.h`
and change problem size.
Blocking definitions are located on `stencil_common.h` too.

### Specific information for KNC:

For compiling:
`make arch=knc`

And use `knc_target=<device number>` for running the tests on specific KNC device.
For example, to run on device mic0:
`make arch=knc knc_target=0 run_selftest`

### Contact Info:

email: openvec@gmail.com

