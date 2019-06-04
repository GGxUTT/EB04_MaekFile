SKIN=alchemy
MAIN_SRC=cyclic_test
TARGET=cyclic_test

LM=-lm

### Default Xenomai installation path
XENO ?= /usr/xenomai

XENO_CONFIG=$(shell PATH=$(XENO):$(XENO)/bin:$(PATH) which xeno-config 2>/dev/null)

CFLAGS := $(shell $(XENO_CONFIG) --skin=alchemy --cflags)
LDFLAGS := $(LM) $(shell $(XENO_CONFIG) --skin=alchemy --ldflags)
CC := $(shell $(XENO_CONFIG) --cc)

$(TARGET): $(MAIN_SRC).c
	$(CC) -o $@ $< $(CFLAGS) $(LDFLAGS)


	


