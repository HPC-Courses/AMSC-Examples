############################################################
#
# An example of Makefile for the course on 
# Advanced Programming for Scientific Computing
# It should be modified for adapting it to the various examples
#
############################################################
#
# The environmental variable AMSC_ROOT should be set to the
# root directory where the examples reside. In practice, the directory
# where this file is found. The resolution of AMSC_ROOT is made in the
# Makefile.h file, where other important variables are also set.
# The only user defined variable that must be set in this file is
# the one indicating where Makefile.h resides

MAKEFILEH_DIR=../../
#
include $(MAKEFILEH_DIR)/Makefile.inc
#
# You may have an include file also in the current directory
#
-include Makefile.inc

#
# The general setting is as follows:
# mains are identified bt main_XX.cpp
# all other files are XX.cpp
#

# get all files *.cpp
SRCS=$(wildcard *.cpp)
# get the corresponding object file
OBJS = $(SRCS:.cpp=.o)
# get all headers in the working directory
HEADERS=$(wildcard *.hpp)
#
exe_sources=$(SRCS)
EXEC=test_tuple test_tie test_tuple_cat tuple1

#========================== ORA LA DEFINIZIONE DEGLI OBIETTIVI
.phony= all  clean

all: $(DEPEND) $(EXEC)

clean:
	-\rm -f $(EXEC) $(OBJS)

distclean:
	$(MAKE) clean
	-\rm -r -f ./doc
	-\rm *.out *.bak *~

doc:
	doxygen $(DOXYFILE)


$(OBJS): $(SRCS)

$(DEPEND): $(SRCS)
	$(CXX) $(CPPFLAGS) $(CXXFLAGS) -MM $(SRCS) -MF $(DEPEND)



-include $(DEPEND)




