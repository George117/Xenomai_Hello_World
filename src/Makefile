XENO_CONFIG := /usr/xenomai/bin/xeno-config
CFLAGS := $(shell $(XENO_CONFIG) --cobalt --cflags)
LDFLAGS := $(shell $(XENO_CONFIG) --cobalt --ldflags)
CC := $(shell $(XENO_CONFIG) --cc)

INCLUDE = -I/usr/xenomai/include
EXECUTABLE := hello_world

all: $(EXECUTABLE)

%: %.c
	$(CC) -o $@ $< $(CFLAGS) $(LDFLAGS) $(INCLUDE)

clean:
	rm hello_world
