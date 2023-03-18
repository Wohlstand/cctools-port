bin_PROGRAMS =  \
	dyldinfo \
	ObjectDump \
	unwinddump \
	machocheck
#	rebase

AM_CXXFLAGS = \
	-D__DARWIN_UNIX03 \
	$(WARNINGS) \
	-Wno-switch \
	$(LTO_DEF) \
	$(ENDIAN_FLAG) \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/include/foreign \
	-I$(top_srcdir)/ld64-ppc/src \
	-I$(top_srcdir)/ld64-ppc/src/3rd \
	-I$(top_srcdir)/ld64-ppc/src/abstraction \
	-I$(top_srcdir)/ld64-ppc/src/ld \
	-I$(top_srcdir)/ld64-ppc/src/ld/parsers \
	-I$(top_srcdir)/ld64-ppc/src/ld/passes

AM_CFLAGS = \
	-D__DARWIN_UNIX03 \
	$(WARNINGS) \
	$(LTO_DEF) \
	$(ENDIAN_FLAG) \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/include/foreign \
	-I$(top_srcdir)/ld64-ppc/src \
	-I$(top_srcdir)/ld64-ppc/src/3rd \
	-I$(top_srcdir)/ld64-ppc/src/abstraction \
	-I$(top_srcdir)/ld64-ppc/src/ld \
	-I$(top_srcdir)/ld64-ppc/src/ld/parsers \
	-I$(top_srcdir)/ld64-ppc/src/ld/passes

unwinddump_SOURCES = unwinddump.cpp

machocheck_SOURCES = machochecker.cpp
machocheck_LDADD = $(top_builddir)/ld64-ppc/src/3rd/libhelper.la

#rebase_SOURCES = rebase.cpp
#rebase_LDADD = \
#	$(top_builddir)/ld64-ppc/src/ld/parsers/libParsers.la \
#	$(LTO_RPATH) \
#	$(LTO_LIB) \
#	$(DL_LIB)

ObjectDump_SOURCES = \
	ObjectDump.cpp \
	$(top_srcdir)/ld64-ppc/src/ld/debugline.c

ObjectDump_LDADD =  \
	$(top_builddir)/ld64-ppc/src/ld/parsers/libParsers.la \
	$(top_builddir)/ld64-ppc/src/3rd/BlocksRuntime/libBlocksRuntime.la  \
	$(LTO_RPATH) \
	$(LTO_LIB) \
	$(DL_LIB)

dyldinfo_SOURCES = dyldinfo.cpp
dyldinfo_LDADD = $(top_builddir)/ld64-ppc/src/3rd/libhelper.la
