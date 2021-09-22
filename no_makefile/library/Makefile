CC:=gcc
CFLAGS:=-fPIC -Wall

LDFLAGS:=-shared
LIB:=libfilereader.so
LNAME:=lfilereader
LIBSRC:=file_reader.c
LIBHEADER:=$(LIBSRC:.c=.h)

BIN=no_makefile_reader
BINSRC:=main.c

DESTDIR:=/usr

all: $(LIB) $(BIN)

$(LIB): 
	$(CC) $(CFLAGS) -o $@ $(LDFLAGS) $(LIBSRC)

$(BIN):
	$(CC) $(CFLAGS) -o $@ $(BINSRC) -I$(PWD) -L$(PWD) -$(LNAME)


install: $(LIB) $(BIN)
	install -m 644 $(LIBHEADER) $(DESTDIR)/include
	install -m 644 $(LIB) $(DESTDIR)/lib
	install -m 555 $(BIN) $(DESTDIR)/bin/

uninstall:
	$(RM) $(DESTDIR)/include/$(LIBHEADER)
	$(RM) $(DESTDIR)/lib/$(LIB)
	$(RM) $(DESTDIR)/bin/$(BIN)

clean:
	$(RM) $(BIN) $(LIB)