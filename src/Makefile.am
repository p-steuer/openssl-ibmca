VERSION = 2:1:1

lib_LTLIBRARIES=ibmca.la

ibmca_la_SOURCES=e_ibmca.c \
				 e_ibmca_err.c \
				 ibmca_cipher.c \
				 ibmca_digest.c \
				 ibmca_rsa.c \
				 ibmca_dsa.c \
				 ibmca_dh.c \
				 ibmca_ec.c \
				 ibmca_pkey.c

ibmca_la_LIBADD=-ldl
ibmca_la_LDFLAGS=-module -version-number ${VERSION} -shared -no-undefined \
		  -avoid-version -Wl,--version-script=${srcdir}/../ibmca.map

dist_ibmca_la_SOURCES=ibmca.h e_ibmca_err.h
EXTRA_DIST = openssl.cnf.sample

ACLOCAL_AMFLAGS = -I m4
SUBDIRS = doc
