CXX = g++
CXXFLAGS = -g3 -Wall -Wextra -Wconversion -Wcast-align -g -fsanitize=address

.PHONY: all clean format

all: 502sh

format:
	clang-format -style=Google -i *.cpp

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

502sh: sh.o builtin.o
	$(CXX) $(CXXFLAGS) $^ -o $@

clean:
	rm -f 502sh *.o
