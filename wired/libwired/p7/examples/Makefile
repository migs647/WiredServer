# Makefile.in

abs_top_srcdir	= /Users/migs647/Developer/Wired/WiredServer/wired/libwired
rundir			= ../../../run/libwired

DEFS			= -DHAVE_CONFIG_H
CC				= gcc
CFLAGS			= -g -O2
CPPFLAGS		= -I/Users/migs647/Developer/Wired/WiredServer/Pods/OpenSSL-Universal/include-macos -I/usr/local/include -DWI_CORESERVICES -DWI_CARBON -DWI_DIGESTS -DWI_CIPHERS -DWI_PTHREADS -DWI_LIBXML2 -DWI_PLIST -DWI_SQLITE3 -DWI_RSA -DWI_ZLIB -DWI_P7
LDFLAGS			= -L$(rundir)/lib -L/Users/migs647/Developer/Wired/WiredServer/Pods/OpenSSL-Universal/lib-macos -L/usr/local/lib
LIBS			= -lwired -framework CoreServices -framework Carbon -lxml2 -lsqlite3 -lcrypto -lz
INCLUDES		= -I$(abs_top_srcdir) -I$(rundir)/include

COMPILEANDLINK	= $(CC) $(DEFS) $(INCLUDES) $(CPPFLAGS) $(CFLAGS) $(LDFLAGS) -o $@

wiredclient: wiredclient.c
	$(COMPILEANDLINK) $(LIBS) $<
