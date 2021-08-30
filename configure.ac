#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([packETH], [3.0.0], [jemcek@gmail.com])
AC_CONFIG_SRCDIR([src/main.c])
AM_INIT_AUTOMAKE([subdir-objects -Wall])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CC
AM_PROG_CC_C_O
AC_PROG_INSTALL

# Checks for libraries.
AC_CHECK_LIB([m], [pow])
AC_CHECK_LIB([pthread], [pthread_create])

# Checks for header files.
AC_CHECK_HEADER_STDBOOL
AC_CHECK_HEADERS([fcntl.h libintl.h netdb.h arpa/inet.h netinet/in.h stdlib.h string.h sys/ioctl.h sys/socket.h sys/time.h sys/timeb.h unistd.h])

# Check for C internals
AC_C_INLINE
AC_TYPE_INT32_T
AC_TYPE_SSIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T

# We need GTK
PKG_CHECK_MODULES([GTK3], [gtk+-3.0 glib-2.0 gthread-2.0])

# Checks for library functions.
AC_FUNC_ERROR_AT_LINE
AC_FUNC_MALLOC
AC_FUNC_STRTOD
AC_CHECK_FUNCS([bzero ftime clock_gettime gettimeofday isascii memset socket strchr strdup strstr strtol strtoul strtoull])

AC_CONFIG_FILES([Makefile src/Makefile])

# Option to define a larger (or smaller) maximum MTU
AC_ARG_WITH([mtu], [AS_HELP_STRING([--with-mtu], [change the maximum MTU, default: 9000])])
AS_IF([test "x$with_mtu" != "x"],
	[AC_DEFINE_UNQUOTED([MAX_MTU], [${with_mtu}], ["..."])],
	[AC_DEFINE_UNQUOTED([MAX_MTU], [9000], ["..."])])
AS_IF([test "x$with_mtu" != "x"],
	[AC_DEFINE_UNQUOTED([MAX_MTU_STR], ["${with_mtu}"], ["..."])],
	[AC_DEFINE_UNQUOTED([MAX_MTU_STR], ["9000"], ["..."])])

AC_OUTPUT
