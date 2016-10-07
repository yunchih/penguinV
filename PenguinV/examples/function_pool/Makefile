
PWD      := $(shell pwd)
LIB_DIR  := $(PWD)/../../Library
TARGET   := example

CXX      := g++
LINKER   := g++
INCDIRS  := -I$(PWD) -I$(LIB_DIR)
LINKLIBS := -pthread
CXXFLAGS := -std=c++11 -Wall -O2

SRCS := example_function_pool.cpp
LIBS := $(LIB_DIR)/image_function.cpp $(LIB_DIR)/thread_pool.cpp $(LIB_DIR)/function_pool.cpp

all: $(TARGET)

$(TARGET): $(LIBS) $(SRCS)
	$(CXX) $(CXXFLAGS) $(LINKLIBS) $(INCDIRS) $^ -o $@

run: $(TARGET)
	@echo "Running example ..."
	@./$(TARGET)

clean:
	@rm -rf $(TARGET)

