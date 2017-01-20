AC_PREREQ(2.69)
AC_INIT([Ada Scratch Space], [0.1.0], [ronald.dahlgren@gmail.com],, [http://dahlgren.work])

AM_INIT_AUTOMAKE
AC_USE_SYSTEM_EXTENSIONS
AC_CONFIG_SRCDIR([src/main.c])
AC_CONFIG_HEADERS([config.h])

# Point to the extra macros we're using
AC_CONFIG_MACRO_DIR([m4/])

# Verify the compile and install script are present
AC_PROG_CC([gcc])
AC_PROG_INSTALL
AC_PROG_RANLIB

##########################################
# Check for various GNAT installations
##########################################

# The user must have at least an operation native GNAT Ada compiler

AM_PROG_WORKING_ADA

AM_PROG_GNATMAKE
AM_PROG_WORKING_ADA
AC_CHECK_PROG(GNATCLEAN, gnatclean, gnatclean)


AC_CONFIG_FILES([Makefile
                  README
                  src/ch1/Makefile
                  src/Makefile])
AC_OUTPUT

echo \
"-------------------------------------------------

 ${PACKAGE_NAME} Version ${PACKAGE_VERSION}

 Prefix: '${prefix}'.
 Compiler: '${CC} ${CFLAGS} ${CPPFLAGS}'

 Now type 'make @<:@<target>@:>@'
   where the optional <target> is:
     all                - build all binaries (default)
     install            - install everything

--------------------------------------------------"
