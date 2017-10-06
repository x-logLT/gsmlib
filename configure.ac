#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT(gsmlib, 1.10, https://github.com/vbouchaud/gsmlib)
AC_CONFIG_SRCDIR([gsm_config.h.in])
AC_CONFIG_HEADERS([gsm_config.h])
AC_CONFIG_MACRO_DIRS([m4])
AM_INIT_AUTOMAKE

GSM_VERSION="1:4:0"
AC_SUBST(GSM_VERSION)

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC
AC_PROG_CPP
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET

# Checks for libraries.

LT_INIT

# Checks for header files.
AC_FUNC_ALLOCA
AC_CHECK_HEADERS([argz.h fcntl.h libintl.h limits.h locale.h malloc.h netinet/in.h nl_types.h stddef.h stdlib.h string.h strings.h sys/ioctl.h sys/param.h sys/time.h syslog.h termios.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T

# Checks for library functions.
AC_USE_SYSTEM_EXTENSIONS
AM_GNU_GETTEXT
AC_FUNC_MALLOC
AC_FUNC_MMAP
AC_FUNC_REALLOC
AC_CHECK_SIZEOF([unsigned short int])
AC_CHECK_SIZEOF([unsigned int])
AC_CHECK_SIZEOF([unsigned long int])
AC_CHECK_FUNCS([__argz_count __argz_next __argz_stringify vsnprintf alarm getcwd mempcpy memset munmap putenv select setenv setlocale stpcpy strcasecmp strchr strdup strerror])

AM_CONDITIONAL(COMPILE_INTL, test x$USE_INCLUDED_LIBINTL = xyes)

AC_CONFIG_FILES([Makefile
                 apps/Makefile
                 doc/Makefile
                 ext/Makefile
                 gsmlib/Makefile
                 scripts/Makefile
                 tests/Makefile
                 win32/Makefile
				 po/Makefile.in])
AC_OUTPUT
