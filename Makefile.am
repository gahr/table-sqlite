noinst_PROGRAMS =	table-sqlite

table_sqlite_SOURCES =	table_sqlite.c dict.c log.c table_stdio.c util.c

LDADD =			$(LIBOBJS)

dist_man5_MANS =	table-sqlite.5

smtpdir =		${prefix}/libexec/smtpd

install-exec-local: $(noinst_PROGRAMS)
	$(MKDIR_P) $(DESTDIR)$(smtpdir)
	$(INSTALL_PROGRAM_ENV) $(INSTALL_PROGRAM) $(noinst_PROGRAMS) $(DESTDIR)$(smtpdir)

README.md: table-sqlite.5
	mandoc -Tmarkdown -l table-sqlite.5 > README.md
