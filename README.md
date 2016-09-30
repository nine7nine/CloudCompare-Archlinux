# CloudCompare - Archlinux package

http://www.cloudcompare.org/

https://github.com/cloudcompare/trunk

I'm still tinkering with my pkgbuild and new to Cloudcompare, but there is no proper Archlinux package. So...
Just to keep on top of things, I will upload it on github to work on. 

There are two main folders/source packages;

* cloudcompare-git: archlinux source package for use with GCC

* cloudcompare_ICC-git: Archlinux source package for use with Intel C/C++ Compiler suite

There are currently a few plugins disabled, mostly plugins that require special and/or proprietary SDKs. Aside from that, I have lit up most of the plugins, with only a couple to still get sorted out. I've enabled things like openmp support and ffmpeg support too. 

NOTES:

The two folders/source packages are not needed for building CC, they are for specifc features that aren't enabled.

* vxl-git is not required to compile Cloudcompare; it is however, a dependency for the qGMMREG plugin (currently disabled!)

* blas_icc_git is only for the Intel/icc build, *if" liblas is enabled in the build (currently disabled!). Requires;

-DOPTION_USE_LIBLAS=ON
-DLIBLAS_INCLUDE_DIR=/usr/include
-DLIBLAS_RELEASE_LIBRARY_FILE=/usr/lib/liblas.so

...and liblas_icc-git to be built from source, prior to compiling CC.

liblas-git in AUR is broken on ICC and requires patching, so I have this disabled ~ but have provided
a source package... I am currently using this on my local machine.
