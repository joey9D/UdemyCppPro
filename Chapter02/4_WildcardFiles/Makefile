###############
## VARIABLES ##
###############
DEBUG = 1
EXECUTABLE_NAME = main

CXX = g++
CXX_STANDARD = c++17
CXX_WARNINGS = -Wall -Wextra -Wpedantic
CXXFLAGS = $(CXX_WARNINGS) -std=$(CXX_STANDARD)
CPPFLAGS =
LDFLAGS =

ifeq ($(DEBUG), 1)
CXXFLAGS += -g -O0
else
CXXFLAGS += -O3
endif

COMPILER_CALL = $(CXX) $(CXXFLAGS)

# select all files with the .cc extension
# to see all use echo $(CXX_SOURCES)
CXX_SOURCES = $(wildcard *.cc)

# List of all output .o files
# CXX_OBJECTS = my_lin.o main.o
# patsubst = pattern substitution:
# - use all .cc/.cpp files
# - generate .o files / exchange .cc/.cpp with .o
# - use text of cxx_sources variable
CXX_OBJECTS = $(patsubst %.cc, %.o, $(CXX_SOURCES))

###############
## TARGETS   ##
###############
build: $(CXX_OBJECTS)
	$(COMPILER_CALL) $(CXX_OBJECTS) -o $(EXECUTABLE_NAME)

execute:
	./$(EXECUTABLE_NAME)

clean:
	rm -f *.o
	rm -f $(EXECUTABLE_NAME)

##############
## PATTERNS ##
##############
# $@: the file name of the target
# $<: the name of the first dependency
# file ending/type
%.o: %.cc
    # 				    %.o   %.cc
	$(COMPILER_CALL) -c $< -o $@
