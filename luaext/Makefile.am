noinst_LTLIBRARIES = libluaext.la

EXTRA_DIST = \
	modemuncher.c \
	userconfig.c \
	linit.lua

AM_CPPFLAGS = -I$(top_builddir)
AM_CPPFLAGS += -I$(srcdir)/include -I.

libluaext_la_CPPFLAGS = $(AM_CPPFLAGS) -DWITH_POSIX
libluaext_la_LIBADD = -llua
libluaext_la_SOURCES = \
		linit.h \
		lposix.h \
		lposix.c \
		lrexlib.h \
		lrexlib.c 

linit.lch: linit.lua
	bin2c linit.lua > linit.lch
