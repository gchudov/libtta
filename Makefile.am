AUTOMAKE_OPTIONS = no-dependencies foreign

lib_LIBRARIES = libtta.a

libtta_a_SOURCES = libtta.c libtta.h filter.h

if ENABLE_ASM
if CPU_ARM
EXTRA_libtta_a_SOURCES = filter_arm.S
libtta_a_LIBADD = filter_arm.o
endif
endif

DOCLIST = COPYING README

.PHONY: console

console:
	cd console
	$(MAKE) $(AM_MAKEFLAGS)

SUBDIRS = . console
EXTRA_DIST = config.h Makefile.rm Makefile.mipsel libtta.sln libtta.vcxproj*
