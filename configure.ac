#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ(2.52)

AC_INIT([Apertium Spanish], [1.1.0], [francis.tyers@gmail.com], [apertium-spa], [http://wiki.apertium.org/wiki/Apertium-spa])
AM_INIT_AUTOMAKE

AC_PROG_LN_S
AC_PROG_AWK

m4_define([required_apertium_version], [3.4.0])
m4_define([required_lttoolbox_version], [3.3.2])

PKG_CHECK_MODULES(APERTIUM,   apertium >= required_apertium_version)
PKG_CHECK_MODULES(LTTOOLBOX, lttoolbox >= required_lttoolbox_version)

AC_PATH_PROG([LTPRINT], [lt-print], [false], [$PATH$PATH_SEPARATOR$with_lt_print/bin])
AS_IF([test x$LTPRINT = xfalse], [AC_MSG_ERROR([You don't have lt-print installed])])

AC_PATH_PROG([CGCOMP], [cg-comp], [false], [$PATH$PATH_SEPARATOR$with_cg_comp/bin])
AS_IF([test x$CGCOMP = xfalse], [AC_MSG_ERROR([You don't have cg-comp installed])])

AC_PATH_PROG([CGPROC], [cg-proc], [false], [$PATH$PATH_SEPARATOR$with_cg_proc/bin])
AS_IF([test x$CGPROC = xfalse], [AC_MSG_ERROR([You don't have cg-proc installed])])

AC_PATH_PROG([LRXCOMP], [lrx-comp], [false], [$PATH$PATH_SEPARATOR$with_lrx_comp/bin])
AS_IF([test x$LRXCOMP = xfalse], [AC_MSG_ERROR([You don't have lrx-comp installed])])

AC_PATH_PROG([PKGCONFIG], [pkg-config], [false], [$PATH$PATH_SEPARATOR$with_pkg_config/bin])
AS_IF([test x$PKGCONFIG = xfalse], [AC_MSG_ERROR([You don't have pkg-config installed])])

AP_MKINCLUDE

AC_OUTPUT([Makefile apertium-spa.pc])
