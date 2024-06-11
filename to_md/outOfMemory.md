# Introduction

The Java Runtime Environment, which Autoplot runs within, has the
problem that the amount of memory allocated to it is fixed, and because
of this Autoplot will often encounter an "Out of Memory" error. By
default, Autoplot runs within a 1GB (gigabyte) Java Virtual Machine
(JVM), because this works for both 32bit and 64bit Java Runtime
Environments. So even if the machine has 16GB available to it, the
virtual machine will still only use 1GB.

# What to do when Autoplot runs out of memory

  - run with a 64 bit machine (newer machines are 64bit), with a 64bit
    Java. This is better able to utilize the default 1GB system memory
    available, and is easily increased to more memory.
  - run with more memory with the Java switch -Xmx8GB.
  - launch Autoplot with a bigger JVM with webstart:
    <http://autoplot.org/autoplot.jnlp?max-heap-size=4G>
  - run using the single-jar release, which will now get more memory
    when launched: java -jar autoplot.jar
