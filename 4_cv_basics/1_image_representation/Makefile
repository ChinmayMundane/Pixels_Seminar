<<<<<<< HEAD
CC = g++
CFLAGS = -Wall -Wextra -pedantic -std=c++11
LIBS = -lSDL2

SRCS = image_representation.cpp
OBJS = $(SRCS:.cpp=.o)
TARGET = image
all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o $(TARGET) $(LIBS)

.cpp.o:
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	$(RM) $(OBJS) $(TARGET)
=======
# Specifying which compiler to use
CC = g++							

# Defining the name of the object that will be created after using make
PROJECT = image_representation		

# Here Include specifies which directories can be added in the include path of the main.cpp
CFLAGS = -std=c++11 $(shell pkg-config --cflags opencv4) -Iinclude/		
# What libraries to be imported here it is opencv and SDL
LIBS = $(shell pkg-config --libs opencv4) -lSDL2

# Similar to how we used to link ad make object files in the terminal
# the command make build SRC=<FILENAME> should build the executable in the subfolder
.PHONY: build
ifeq ($(SRC),)
build:
	$(error "SRC is not set")
else
build:
	@echo "Building..."
	@$(CC) $(SRC) -o $(PROJECT) $(CFLAGS) $(LIBS)
endif	

# if folder is not set, clean all build files all subfolders
.PHONY: clean
clean:
	@echo "Cleaning..."
	@rm -rf $(PROJECT)

>>>>>>> 8276e38e424a997a272e839e88ce61e164a89c07
