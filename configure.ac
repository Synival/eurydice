# Define version here, before initialization.
m4_define(eury_version_major, 0)
m4_define(eury_version_minor, 0)
m4_define(eury_version_micro, 1)
m4_define(eury_version, [eury_version_major.eury_version_minor.eury_version_micro])

# Initialize.
AC_PREREQ([2.62])
AC_INIT(eurydice, [eury_version])

# Pass version along to Makefile.
AC_SUBST(EURY_VERSION, [eury_version])
AC_SUBST(EURY_BUILD, [$(git rev-list --count master)])

# AC Configuration.
AC_CONFIG_SRCDIR([src/.dummy])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIRS([m4])

# Configure libtool.
AC_PROG_LIBTOOL

# Configure automake.
AM_INIT_AUTOMAKE([subdir-objects])

# Checks for programs.
AC_PROG_CC
AC_PROG_CC_C99
AC_PROG_RANLIB

# Checks for libraries.

# Checks for header files.
AC_CHECK_HEADERS([stdlib.h string.h stdio.h math.h stdarg.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([memset strchr strdup strcasecmp])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
