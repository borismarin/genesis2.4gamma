AC_PREREQ(2.52)
AC_INIT([genesis], [2.4], [genesis@genesis-sim.org])

# If the user did not supply --prefix, we fail loudly
# (taken from NEST's configure.ac)
if test $prefix = NONE; then
  echo "Please supply a valid installation prefix!"
  echo "GENESIS will then be installed into \$PREFIX/genesis-2.4"
  echo "Example: to install GENESIS into \$HOME/opt/genesis-2.4, run the following:"
  echo "./configure --prefix=\$HOME/opt"
  exit 1
fi

# check for correct compiler & libraries
AC_PROG_CC
AC_PROG_CPP
AC_PATH_X
AC_PATH_XTRA
AC_PROG_RANLIB
AC_PROG_YACC
if test x"$YACC" = "xyacc"; then
  AC_CHECK_PROG([YACC_EXISTS], [yacc], [yes], [no])
  if test x"$YACC_EXISTS" != xyes; then
    AC_MSG_ERROR([[bison|byacc|yacc not found. Please install _bison_ in order to compile Genesis.]])
  fi
fi
AC_PROG_LEX
if test x"$LEX" == x":" ; then
    AC_MSG_ERROR([flex|lex not found. Please install _flex_ in order to compile Genesis.])
fi


AC_CHECK_LIB([ncurses], [main], [], [AC_MSG_ERROR([Missing ncurses.])])

AC_SUBST(X_INC, $x_includes)
AC_SUBST(X_LIB, $x_libraries)
AC_SUBST(LEX, $LEX)
AC_SUBST(LEXLIB, $LEXLIB)

AC_CHECK_SIZEOF([long int])
AS_IF([test "$ac_cv_sizeof_long_int" -eq 8],
    [AC_DEFINE([LONGWORDS])])

AC_OUTPUT(Makefile)
