include $(RTEMS_ROOT)/make/custom/@RTEMS_BSP@.cfg
include $(top_srcdir)/../automake/compile.am

include $(top_srcdir)/ada.am

noinst_PROGRAMS = ada_sp25
ada_sp25_SOURCES = sp25.adb config.h sptest.adb sptest.ads
ada_sp25_SOURCES += init.c

ada_sp25$(EXEEXT): sp25.adb init.$(OBJEXT)
	$(GNATCOMPILE) -margs -a $< -o $@

scndir = $(rtems_ada_testsdir)
dist_scn_DATA = ada_sp25.scn

