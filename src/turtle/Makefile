PACKAGE=turtle

MAIN=TurtleSoup
SOURCES=Action.java DrawableTurtle.java LineSegment.java PenColor.java Point.java TurtleGUI.java Turtle.java TurtleSoup.java
TESTS=TurtleSoupTest
TEST_SOURCES=$(foreach t,$(TESTS),$(t).java)

JAVA=java
JAVAC=javac
JAVAC_FLAGS=
CLASSPATH=/usr/share/java/junit.jar:/usr/share/java/junit4.jar:.
JUNIT_CORE=org.junit.runner.JUnitCore
JUNIT_FLAGS=-ea

all:
	$(JAVAC) -cp $(CLASSPATH) $(JAVAC_FLAGS) $(SOURCES) $(TEST_SOURCES)

run: all
	(cd .. && $(JAVA) -cp $(CLASSPATH) $(PACKAGE).$(MAIN))

test: all $(TESTS)

$(TESTS): %:
	(cd .. && $(JAVA) -cp $(CLASSPATH) $(JUNIT_FLAGS) $(JUNIT_CORE) $(PACKAGE).$@)

clean:
	rm -rf *.class
