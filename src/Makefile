JC = javac
JVM = java
PACKAGE = jlox
MAIN = jlox.Lox
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
	@echo "Running $(MAIN_CLASS)..."
	@$(JVM) -cp $(DEST) $(MAIN)

clean:
	$(RM) $(DEST)/*.class

.PHONY: jlox run default clean