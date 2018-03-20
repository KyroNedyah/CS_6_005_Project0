PACKAGE=rules

SOURCES=RulesOf6005.java
TESTS=RulesOf6005Test
TEST_SOURCES=$(foreach t,$(TESTS),$(t).java)

JAVA=java
JAVAC=javac
JAVAC_FLAGS=
CLASSPATH=/usr/share/java/junit.jar:/usr/share/java/junit4.jar:.
JUNIT_CORE=org.junit.runner.JUnitCore

all:
	$(JAVAC) -cp $(CLASSPATH) $(JAVAC_FLAGS) $(SOURCES) $(TEST_SOURCES)

test: $(TESTS)

$(TESTS): %:
	(cd .. && $(JAVA) $(JUNIT_CORE) $(PACKAGE).$@)

clean:
	rm -rf *.class
