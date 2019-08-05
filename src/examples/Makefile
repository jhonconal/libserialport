#指定交叉编译工具链
CROSS_COMPILE =
AS       = $(CROSS_COMPILE)as  
LD       = $(CROSS_COMPILE)ld  
CC      = $(CROSS_COMPILE)gcc  
CPP    = $(CC) -E  
CXX    =$(CROSS_COMPILE)g++
AR      = $(CROSS_COMPILE)ar  
NM     = $(CROSS_COMPILE)nm
 
#获取工程的根目录的全路径
SOURCE_ROOT = $(shell pwd)

#调用shell脚本，创建静态库文件和执行文件目录
BIN_DIR = $(SOURCE_ROOT)/bin/
# $(shell mkdir -p ${BIN_DIR})

#当前目录和LIB_INC目录下查找原文件
LIB_INC = ../libserial/
INC = -I. -I$(LIB_INC)

TEST_LIB = -L../lib -lserialport

main_page_example_SOURCES = main_page_example.cpp
main_page_example_bin =main_page_example

serial_port_read_SOURCES = serial_port_read.cpp
serial_port_read_bin=serial_port_read

serial_port_read_write_SOURCES = serial_port_read_write.cpp
serial_port_read_write_bin = serial_port_read_write

serial_port_write_SOURCES = serial_port_write.cpp
serial_port_write_bin= serial_port_write

serial_stream_read_SOURCES = serial_stream_read.cpp
serial_stream_read_bin = serial_stream_read

serial_stream_read_write_SOURCES = serial_stream_read_write.cpp
serial_stream_read_write_bin = serial_stream_read_write

serial_stream_write_SOURCES = serial_stream_write.cpp
serial_stream_write_bin = serial_stream_write

EXAMPLE_SRC =  main_page_example.cpp  serial_port_read.cpp \
							 serial_port_read_write.cpp  serial_port_write.cpp  \
							 serial_stream_read.cpp serial_stream_read_write.cpp  \
							 serial_stream_write.cpp

EXAMPLE_BINS  =  main_page_example  serial_port_read \
							 serial_port_read_write  serial_port_write  \
							 serial_stream_read serial_stream_read_write  \
							 serial_stream_write

EXAMPLE_OBJECTS  =  main_page_example.o  serial_port_read.o \
							 serial_port_read_write.o  serial_port_write.o  \
							 serial_stream_read.o serial_stream_read_write.o  \
							 serial_stream_write.o
all:
	$(CXX) $(INC) serial_port_read_write.cpp -o main_page_example -L../lib -lserialport
	$(CXX) $(INC) serial_port_read.cpp -o serial_port_read -L../lib -lserialport
	$(CXX) $(INC) serial_port_read_write.cpp -o serial_port_read_write -L../lib -lserialport
	$(CXX) $(INC) serial_port_write.cpp -o serial_port_write -L../lib -lserialport
# 	$(CXX) $(INC) serial_stream_read.cpp -o serial_stream_read -L../lib -lserialport
#	$(CXX) $(INC) serial_stream_read_write.cpp -o serial_stream_read_write -L../lib -lserialport
#	$(CXX) $(INC) serial_stream_write.cpp -o serial_stream_write -L../lib -lserialport
	
clean:
	- rm -rf *.o  $(BIN_DIR)
