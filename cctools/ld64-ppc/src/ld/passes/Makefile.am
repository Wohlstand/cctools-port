noinst_LTLIBRARIES = libPasses.la
noinst_HEADERS =  \
	branch_island.h \
	branch_shim.h \
	compact_unwind.h \
	dtrace_dof.h \
	dylibs.h \
	got.h \
	huge.h \
	objc.h \
	order_file.h \
	tlvp.h

libPasses_la_LIBADD =  \
	 $(top_builddir)/ld64-ppc/src/3rd/libhelper.la

libPasses_la_CXXFLAGS = \
	-D__DARWIN_UNIX03 \
	$(WARNINGS) \
	$(LTO_DEF) \
	$(ENDIAN_FLAG) \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/include/foreign \
	-I$(top_srcdir)/ld64-ppc/src/abstraction \
	-I$(top_srcdir)/ld64-ppc/src/ld \
	-I$(top_srcdir)/ld64-ppc/src/ld/parsers \
	-I$(top_srcdir)/ld64-ppc/src/3rd \
	-I$(top_srcdir)/ld64-ppc/src

libPasses_la_SOURCES =  \
	branch_island.cpp \
	branch_shim.cpp \
	compact_unwind.cpp \
	dtrace_dof.cpp \
	dylibs.cpp \
	got.cpp \
	huge.cpp \
	objc.cpp \
	order_file.cpp \
	tlvp.cpp \
	stubs/stubs.cpp
