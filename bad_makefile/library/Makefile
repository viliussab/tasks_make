CC:=gcc
CFLAGS:=-fPIC -Wall
LDFLAGS:=-shared
LIB:=libcalculator.so
VER:=1.0

DESTDIR:=/usr

all: $(LIB)$(VER)

$(LIB)$(VER): 
	$(CC) $(CFLAGS) -o $@ $(LDFLAGS) math_functions.c

install: $(LIB)$(VER)
	install -m 644 math_functions.h $(DESTDIR)/include
	install -m 644 $(LIB)$(VER) $(DESTDIR)/lib
	ln -s $(DESTDIR)/lib/$(LIB)$(VER) $(DESTDIR)/lib/$(LIB)

uninstall:
	$(RM) $(DESTDIR)/include/math_functions.h
	$(RM) $(DESTDIR)/lib/$(LIB)
	$(RM) $(DESTDIR)/lib/$(LIB)$(VER)

clean:
	rm -f $(LIB)$(VER)
