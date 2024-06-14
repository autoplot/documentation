Purpose: Outline procedure for adding tests

Audience: Developers of Autoplot

# Introduction

Autoplot's nightly testing has been essential to its development and
acceptable stability. This document covers how tests are created and
added to the nightly tests.

# Jemmy GUI Testing

Jemmy is a Java system that tests GUIs by synthesizing GUI event objects
so that the GUI thinks it is interacting with a human, and the lines of
code between the button clicks and methods callable from scripts are
tested.

Jemmy tests require the Jemmy library be on the Java path, and a special
Jemmy test class is created that will run the test.

## Adding a test

The Jemmy tests are in the SVN repository at
.../autoplot/VATesting/src/org/autoplot/test/. A Jemmy test implements
the org.netbeans.jemmy.Scenario interface, which has a "runIt(Object)"
implementation and a main method that invokes the test with
introspection via org.netbeans.jemmy.Test.main(params) where params is a
String array and params\[0\] is the test name. When copying an existing
test to make a new test, be sure to update the main method.

## Best practices

Now that the benefits of Jemmy are known, there are logical conventions
new GUIs should be created. For example, every component really should
have an internal name, so that the Jemmy tests can get a reference to
them. It's common that old GUIs will need to be modified to support
Jemmy testing, and the name of the GUI should match the name typically
used in the Java source code.

