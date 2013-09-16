INCLUDE := -I../ -I../muduo
SRC_COMM = main.cc \
		echo.cc

OBJ_COMM = $(SRC_COMM:.cpp=.o)

LIBS = ../lib/libmuduo_base.a ../lib/libmuduo_net.a

.SUFFIXES: .o .cpp
.cpp.o:
	g++ $(INCLUDE) -g -c -o $@ $<

PROGRAM = test
all: test
        
test: $(OBJ_COMM)  
	g++ -o $@ $(INCLUDE) $(OBJ_COMM) $(LIBS) -lpthread -lrt 
	
clean: 
	rm -f *.o
