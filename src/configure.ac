AC_INIT(genesis, version-2.4g)

AC_PROG_CC
AC_PROG_CPP
AC_PATH_X 
AC_PATH_XTRA
AC_PROG_LEX
AC_PROG_YACC
AC_PROG_RANLIB

AC_CHECK_LIB([ncurses], [main], [], [AC_MSG_ERROR([Missing ncurses.])])

AC_SUBST(X_INC, $x_includes)
AC_SUBST(X_LIB, $x_libraries)
AC_SUBST(LEX, $LEX)
AC_SUBST(LEXLIB, $LEXLIB)

AC_CHECK_SIZEOF([long int]) 
AS_IF([test "$ac_cv_sizeof_long_int" -eq 8], 
    [AC_DEFINE([LONGWORDS])])

AC_OUTPUT(Makefile)
