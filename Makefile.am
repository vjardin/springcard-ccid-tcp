ACLOCAL_AMFLAGS = -I m4

SUBDIRS = readers src

EXTRA_DIST = bootstrap ChangeLog SCARDGETATTRIB.txt \
	$(AUX_DIST) \
	m4/ax_pthread.m4 \
	MacOSX/configure \
	MacOSX/convert_reader_h.pl \
	MacOSX/debuglog.h \
	MacOSX/ifdhandler.h \
	MacOSX/pcsclite.h \
	MacOSX/reader.h \
	MacOSX/winscard.h \
	MacOSX/wintypes.h

MAINTAINERCLEANFILES = $(AUX_DIST)
DISTCLEANFILES = ChangeLog

# Automatically update the libtool script if it becomes out-of-date.
LIBTOOL_DEPS = @LIBTOOL_DEPS@
libtool: $(LIBTOOL_DEPS)
	$(SHELL) ./config.status --recheck

ChangeLog:
	git2cl > $@

