AM_CPPFLAGS += $(PGSQL_inc)
pkglib_LTLIBRARIES = libgpgsqlbackend.la

EXTRA_DIST = \
	OBJECTFILES \
	OBJECTLIBS \
	dnssec-3.x_to_3.4.0_schema.pgsql.sql
	nodnssec-3.x_to_3.4.0_schema.pgsql.sql \
	schema.pgsql.sql

dist_doc_DATA = \
	schema.pgsql.sql \
	nodnssec-3.x_to_3.4.0_schema.pgsql.sql \
	dnssec-3.x_to_3.4.0_schema.pgsql.sql

libgpgsqlbackend_la_SOURCES = \
	gpgsqlbackend.cc gpgsqlbackend.hh \
	spgsql.cc spgsql.hh

libgpgsqlbackend_la_LDFLAGS = -module -avoid-version
libgpgsqlbackend_la_LIBADD = $(PGSQL_lib) -lssl $(LIBCRYPT) -lcrypto
