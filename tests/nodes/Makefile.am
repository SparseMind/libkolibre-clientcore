## Copyright (C) 2012 Kolibre
#
# This file is part of kolibre-clientcore.
#
# Kolibre-clientcore is free software: you can redistribute it and/or modify
# it under the terms of the GNU Lesser General Public License as published by
# the Free Software Foundation, either version 2.1 of the License, or
# (at your option) any later version.
#
# Kolibre-clientcore is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU Lesser General Public License for more details.
#
# You should have received a copy of the GNU Lesser General Public License
# along with kolibre-clientcore. If not, see <http://www.gnu.org/licenses/>.
#

AUTOMAKE_OPTIONS = foreign

check_PROGRAMS = rootnode filesystemnode daisybooknode daisyonlinebooknode daisyonlinenode daisynavi

TESTS = rootnode filesystemnode daisybooknode.sh daisyonlinebooknode.sh daisyonlinenode.sh daisynavi.sh

rootnode_SOURCES = rootnode.cpp
filesystemnode_SOURCES = filesystemnode.cpp
daisybooknode_SOURCES = daisybooknode.cpp
daisyonlinebooknode_SOURCES = daisyonlinebooknode.cpp
daisyonlinenode_SOURCES = daisyonlinenode.cpp
daisynavi_SOURCES = daisynavi.cpp
daisynavi_CPPFLAGS = -I$(top_srcdir)/src @LIBKOLIBRENARRATOR_CFLAGS@ @LIBKOLIBREPLAYER_CFLAGS@ @LIBKOLIBREXMLREADER_CFLAGS@ @LIBKOLIBREAMIS_CFLAGS@ @LIBKOLIBRENAVIENGINE_CFLAGS@

LDADD = $(top_builddir)/src/libkolibre-clientcore.la
AM_LDFLAGS = -L$(top_builddir)/src @LOG4CXX_LIBS@ @LIBKOLIBREPLAYER_LIBS@ @LIBKOLIBRENAVIENGINE_LIBS@ @LIBKOLIBREDAISYONLINE_LIBS@ -lboost_regex -lboost_filesystem -lboost_system
AM_CPPFLAGS = -I$(top_srcdir)/src @LIBKOLIBRENAVIENGINE_CFLAGS@ @LIBKOLIBREDAISYONLINE_CFLAGS@

EXTRA_DIST = \
	daisybooknode.sh \
	daisyonlinebooknode.sh \
	daisyOnlineBookNode \
	daisyonlinenode.sh \
	daisyOnlineNode \
	daisynavi.sh \
	testdata \
	run

clean-local: clean-local-check
.PHONY: clean-local-check

clean-local-check:
	-rm -rf *.order
