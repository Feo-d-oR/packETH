## Process this file with automake to produce Makefile.in

## Place generated object files (.o) into the same directory as their source
## files, in order to avoid collisions when non-recursive make is used.
AUTOMAKE_OPTIONS = subdir-objects

## Additional flags to pass to aclocal when it is invoked automatically at
## make time. The ${ACLOCAL_FLAGS} variable is picked up from the environment
## to provide a way for the user to supply additional arguments.
ACLOCAL_AMFLAGS = ${ACLOCAL_FLAGS}

## Set the default command-line flags for the C preprocessor to the value
## obtained from pkg-config via PKG_CHECK_MODULES in configure.ac.  These
## flags are passed to the compiler for both C and C++, in addition to the
## language-specific options.
## Append to CFLAGS.  Used by gcc to compile c programs
AM_CFLAGS = $(GTK3_CFLAGS) \
	-std=gnu11 \
        -DPACKAGE_DATA_DIR=$(datadir) \
        -DPACKAGE_LOCALE_DIR=$(prefix)/$(DATADIRNAME)/locale \
        -DPKGDATADIR=$(pkgdatadir)/ \
	-g \
	-O2 \
	-Wall \
	-Wmissing-prototypes \
	-Wmissing-declarations \
	-Wunused \
	$(PACKAGE_CFLAGS)

bin_PROGRAMS = packeth_3.0.0

packeth_3_0_0_SOURCES = \
	main.c \
	support.c \
	callbacks.c \
	function.c \
	function_send.c \
	loadpacket.c \
	savepacket.c

packeth_3_0_0_LDADD = $(PACKAGE_LIBS) $(INTLLIBS) $(GTK3_LIBS)
