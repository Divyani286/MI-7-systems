# the name of the target program
TARGET = client
TARGET2 = server

# other source files and the associated object files (this can be blank)
SRC	= client.c
SRC2 = server.c

OBJ	= $(SRC:.c=.o)
OBJ2 = $(SRC2:.c=.o)

# special include directories
INCLUDE = -I.

# special libraries (none for now)
LIB	=

# select the compiler and flags
CC = /usr/bin/gcc
CFLAGS = -g

# .SUFFIXES: .c

# specify how to compile the .c files
.c.o:
	$(CC) $(CFLAGS) $(INCLUDE) -c $<

# if you type 'make' without arguments, this is the default
build: $(TARGET) $(TARGET2)

# specify how to compile the target
$(TARGET): $(OBJ)
	$(CC) $(CFLAGS) $(INCLUDE)  $(OBJ) $(LIB) -o $(TARGET)

$(TARGET2): $(OBJ2)
	$(CC) $(CFLAGS) $(INCLUDE)  $(OBJ2) $(LIB) -o $(TARGET2)


# remove binaries
clean:
	rm -f $(OBJ) $(OBJ2) $(TARGET) $(TARGET2)

# remove binaries and other junk
clobber:
	make clean
	rm -f core *~
