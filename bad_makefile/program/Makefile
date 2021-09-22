CC:=gcc
CFLAGS:=-Wall -Ipwd
OBJS:=main.o math_functions.o
BIN:=calculator

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) -o $@ $^

%.o:%.c
	$(CC) $(CFLAGS) -c -o $@ $^

clean:
	$(RM) $(BIN) $(OBJS) 
