JC = javac
JVM = java
PACKAGE = jlox
MAIN = Lox
DEST = jlox_d

SOURCES = $(wildcard $(PACKAGE)/*.java)
CLASSES = $(SOURCES:.java=.class)

%.class: %.java
	$(JC) -d $(DEST) $(JFLAGS) $<

jlox: $(CLASSES)
	echo "building jlox"
	$(JC) -d $(DEST) $(PACKAGE)/Lox.java

default: jlox

run: jlox
	$(JVM) $(PACKAGE)/$(MAIN)

clean:
	$(RM) *.class

.PHONY: jlox run default clean