# Set the libraries to link
LFLAGS += -lpcap -pthread -lcurl
#CFLAGS += -O2 -s -lm
# Debug
CFLAGS += -g -lm

# The target
TARGET = zoopig
# Object files
OBJECTS = zoopig.o cjson.o handler_config.o curl_handler.o

all: $(TARGET)

$(TARGET): $(OBJECTS)
	$(CC) -o $(TARGET) $(OBJECTS) $(CFLAGS) $(LFLAGS)

# Dependencies:

#radiotap.o: radiotap.h radiotap_iter.h platform.h




# This is a predefined rule of makefile, it knows the dependencies and thus can compile the related ".c" files in to ".o"
# The macro $< means "the first suffix of current target", i.e. ".c"
.c.o:
	$(CC) $(CFLAGS) -c $<

clean:
	rm *.o
	rm $(TARGET)
