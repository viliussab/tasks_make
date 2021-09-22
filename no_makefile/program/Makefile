CC:=gcc
CFLAGS:=-Wall -Ipwd
SRC:=$(wildcard *.c)
OBJ:=$(SRC:.c=.o)
BIN:=calculator

all: $(BIN)

$(BIN): $(OBJ)
	$(CC) $(CFLAGS) -o $@ $^

%.o:%.c
	$(CC) $(CFLAGS) -c -o $@ $^

clean:
	$(RM) $(BIN) $(OBJ) 