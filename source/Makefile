SDK=../../AnalyzerSDK
DYLIB=libISO7816Analyzer.dylib

SRCS=ISO7816Pps.cpp SaleaeHelper.cpp Convert.cpp Logging.cpp iso7816Analyzer.cpp iso7816AnalyzerResults.cpp iso7816AnalyzerSettings.cpp iso7816SimulationDataGenerator.cpp
GDB=-g -ggdb

CFLAGS=-I"$(SDK)/include" -I. -O3 -w -c -fpic -Wall $(GDB)
LDFLAGS=-L/Applications/Logic.app/Contents/MacOS  -lAnalyzer -dynamiclib  $(GDB)
OBJECTS=$(SRCS:.cpp=.o)
CC=g++

all: clean $(OBJECTS) $(DYLIB) Makefile

clean:
	rm -f $(OBJECTS) $(DYLIB)

.cpp.o:
	$(CC) $(CFLAGS) $< -o $@

$(DYLIB): $(OBJECTS)
	$(CC) $(LDFLAGS) -o $(DYLIB) $(OBJECTS)

install:
	cp libISO7816Analyzer.dylib /Applications/Logic.app/Contents/Resources/Analyzers/
