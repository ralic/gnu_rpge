#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.
AC_INIT([rpge], [NOTVERSIONNEDPACKAGE])
#AC_INIT(configure.in)
#AM_INIT_AUTOMAKE([rpge],[NOTVERSIONNEDPACKAGE],[sebastien.diaz@gmail.com])
AC_CONFIG_SRCDIR([src/main.c])
AC_CONFIG_HEADER([config.h])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE
# Checks for programs.
AC_PROG_CC_STDC
#AC_PROG_RANLIB

#Necessary GNUlib macro invocation
gl_EARLY

# Checks for libraries.
AC_CHECK_LIB(SDL, SDL_Init,[],[echo 'Required library libSDL not found.'; exit])
AC_CHECK_LIB(SDL_image, IMG_Load,[],[echo 'Required library libSDL_image not found'; exit])
AC_CHECK_LIB(guile, scm_init_guile,[],[echo 'Required library libguile not found'; exit])
AC_CHECK_LIB(SDL_ttf, TTF_FontHeight,[],[echo 'Required library libSDL_ttf not found'; exit])
#GNUlib
gl_INIT

LT_INIT

# Checks for header files.
AC_CHECK_HEADERS(SDL/SDL.h SDL/SDL_image.h SDL/SDL_ttf.h libguile.h)
# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.
AC_CHECK_FUNCS([memset strdup calloc])
AC_FUNC_MALLOC
AC_FUNC_REALLOC

AC_CONFIG_FILES(Makefile lib/Makefile scm/Makefile doc/Makefile images/Makefile src/Makefile conf/Makefile examples/Makefile)
AC_OUTPUT
