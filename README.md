# CloudCompare - Archlinux package

http://www.cloudcompare.org/

https://github.com/cloudcompare/trunk

I'm still tinkering with my pkgbuild and new to Cloudcompare, but there is no proper Archlinux package. So...
Just to keep on top of things, I will upload it on github to work on. 

There are two main folders/source packages;

* cloudcompare-git: archlinux source package for use with GCC

* cloudcompare_ICC-git: Archlinux source package for use with Intel C/C++ Compiler suite

Both packages enable all plugins, minus; qDUMMY, qKINECT and qMMREG...

* the 'dummy' plugin would never be enabled, since it is an example plugin.
* qKINECT won't be enabled due to not being able to get it's dependencies to build on Archlinux
* qMMREG may be enabled, whenever I have time to figure out out the current issues that are stopping it from building.
