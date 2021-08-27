## Process this file with automake to produce Makefile.in

INCLUDES = \
	-DPACKAGE_DATA_DIR=\""$(datadir)"\" \
	-DPACKAGE_LOCALE_DIR=\""$(prefix)/$(DATADIRNAME)/locale"\" \
	@PACKAGE_CFLAGS@

bin_PROGRAMS = packeth-2.2.1

packeth_2.2.1_SOURCES = \
	main.c \
	support.c support.h \
	callbacks.c callbacks.h

packeth_2.2.1_LDADD = @PACKAGE_LIBS@ $(INTLLIBS)

