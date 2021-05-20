# A simple Makefile for compiling small projects

# set the compiler
CC := g++

# set the compiler flags
DEBUG_FLAGS = -g -O0 -DDEBUG -pthread -I include/
CFLAGS = $(DEBUG_FLAGS) -Wall

# add header files here
HDR1 := 

# add source files here
SRC1 := src/tracker.c

# generate names of object files
OBJ1 := $(SRC1:.c=.o)

# add header files here
HDR2 := 

# add source files here
SRC2 := src/peer.c

# generate names of object files
OBJ2 := $(SRC2:.c=.o)

# name of executable
EXEC1 := tracker

# name of second executable
EXEC2 := peer

# default recipe
all: clean $(EXEC1) $(EXEC2)

# recipe for building the final executable number 1
$(EXEC1): $(OBJ1) $(HDR1) tracker
	$(CC) -o $@ $(OBJ1) $(CFLAGS)

# recipe for building the final executable number 2
$(EXEC2): $(OBJ2) $(HDR2) peer
	$(CC) -o $@ $(OBJ2) $(CFLAGS)

# recipe to clean the workspace
clean:
	rm -f $(wildcard *.o) $(wildcard object/*.o) $(wildcard src/*.o) $(EXEC1) $(EXEC2)
