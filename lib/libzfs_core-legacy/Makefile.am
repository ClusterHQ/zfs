include $(top_srcdir)/config/Rules.am

DEFAULT_INCLUDES += \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/lib/libspl/include

lib_LTLIBRARIES = libzfs_core_legacy.la

USER_C = \
	libzfs_core.c

KERNEL_C =

nodist_libzfs_core_legacy_la_SOURCES = \
	$(USER_C) \
	$(KERNEL_C)

libzfs_core_legacy_la_LIBADD = \
	-lpthread \
	$(top_builddir)/lib/libnvpair/libnvpair.la \
	$(top_builddir)/lib/libzpool/libzpool.la

libzfs_core_legacy_la_LDFLAGS = -version-info 0:0:0

EXTRA_DIST = $(USER_C)
