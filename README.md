# CloudCompare - Archlinux package

http://www.cloudcompare.org/

https://github.com/cloudcompare/trunk

I'm still tinkering with my pkgbuild and new to Cloudcompare, but there is no proper Archlinux package. So...
Just to keep on top of things, I will upload it on github to work on. 

There are two main folders/source packages;

* cloudcompare-git: archlinux source package for use with GCC

* cloudcompare_ICC-git: Archlinux source package for use with Intel C/C++ Compiler suite

There are currently a few plugins disabled, mostly plugins that require special and/or proprietary SDKs. Aside from that, I have lit up most of the plugins, with only a couple to still get sorted out and working. Here is a current list (from my source packages) for cmake;

  cmake .. \
   	  -DCMAKE_BUILD_TYPE=Release \
		  -DCMAKE_INSTALL_PREFIX=/usr \
		  -DBUILD_QPCL_PLUGIN_DOCUMENTATION=ON \
		  -DOPTION_USE_DXF_LIB=ON \
		  -DOPTION_USE_SHAPE_LIB=ON \
		  -DOPTION_USE_GDAL=ON \
		  -DFFMPEG_LIBRARY_DIR=/usr/lib \
		  -DFFMPEG_INCLUDE_DIR=/usr/include \
 		  -DWITH_FFMPEG_SUPPORT=YES \
		  -DCOMPILE_CC_CORE_LIB_WITH_CGAL=ON \
      -DINSTALL_QPCL_PLUGIN=ON \
		  -DINSTALL_QSRA_PLUGIN=ON \
		  -DINSTALL_QCSF_PLUGIN=ON \
		  -DINSTALL_QCSV_MATRIX_IO_PLUGIN=ON \
		  -DINSTALL_QPOISSON_RECON_PLUGIN=ON \
  	  -DPOISSON_RECON_WITH_OPEN_MP=ON \
		  -DINSTALL_QHPR_PLUGIN=ON \
		  -DINSTALL_QRANSAC_SD_PLUGIN=ON \
		  -DINSTALL_QBLUR_PLUGIN=ON \
		  -DINSTALL_QEDL_PLUGIN=ON \
		  -DINSTALL_QPCV_PLUGIN=ON \
		  -DINSTALL_QSSAO_PLUGIN=ON \
		  -DINSTALL_QANIMATION_PLUGIN=ON \
		  -DINSTALL_QFACETS_PLUGIN=ON \
		  -DINSTALL_QHPR_PLUGIN=ON \
		  -DEIGEN_ROOT_DIR=/usr/include/eigen3 \
		  -DNANOFLANN_ROOT_DIR="$srcdir/trunk/plugins/qHoughNormals" \
		  -DINSTALL_QHOUGH_NORMALS_PLUGIN=ON \
		  -DINSTALL_QPHOTOSCAN_IO_PLUGIN=ON \
		  -DINSTALL_QGMMREG_PLUGIN=OFF \
		  -DINSTALL_QKINECT_PLUGIN=OFF \
		  -DINSTALL_QDUMMY_PLUGIN=OFF 
