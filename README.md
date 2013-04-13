
PyModel: Model-based testing in Python
======================================

**PyModel** is an open-source model-based testing framework in Python.

In model-based testing, you code a *model* that can generate as many
test cases as needed.  The model also checks the test outcomes.
Model-based testing is helpful where so many test cases are needed
that it is not feasible to code them all by hand.
 
In the samples included with PyModel, there are models and test
scripts for network sockets, a communication protocol, embedded
controllers, some data structures, a multithreaded application, and a
web application.

PyModel includes an analyzer for validating models, visualizing their
behavior, and checking their safety properties.

PyModel can generate *offline tests* which are similar to unit tests,
but the typical way to use PyModel is *on-the-fly testing*, where the
test runner uses the model to compute the test run as it executes, so
test runs can be as long as needed.  On-the-fly testing can cope with
nondeterminism and asynchrony in the system under test.

PyModel can combine models using *composition*, guide tests through
programmed *scenarios*, and focus test coverage according to
programmed *strategies*.

PyModel provides three main programs:

- **pma**, PyModel analyzer: generates a finite state machine (FSM) 
   and computes properties by exploring a model program, FSM, test suite, 
   or a product of these.
 
- **pmg**, PyModel graphics: generates a file of graphic commands from an FSM,
   that can be processed by the Graphviz *dot* command to produce graphics
   files in various formats including *svg*, *pdf*, and *ps*.
 
- **pmt**, PyModel tester: displays traces, generates tests offline, 
   executes offline tests, or generates and executes tests on-the-fly.

There is also a fourth program:

- **pmv**, PyModel viewer: invokes *pma*, *pmg*, and the Graphiz *dot*
   command (to display the graphics generated by *pmg*).  The *pmv*
   program provides brevity and convenience, so analysis and display
   can be accomplished by a single command.

Use *pma* and *pmg* (or *pmv*) to visualize and preview the behavior of *pmt*.
Every path through the graph created by *pma* (and drawn by *pmg*) is a
trace (test run) that may be generated by *pmt*, when *pma* and *pmt* are
invoked with the same arguments.  The *pma* program is also useful on
its own for visualization and safety analysis.

For more information, read the [notes](notes), browse the
[code](pymodel), peruse the [talks](talks),
or try the [samples](samples).  There are README files in most of the
directories.

PyModel is also available at
[PyPI](http://pypi.python.org/pypi/PyModel).

PyModel requires Python 2.6 or higher (because it uses *itertools.product*)

PyModel is influenced by [NModel](http://www.codeplex.com/NModel), but
is not a translation or re-implementation.

PyModel is covered by the 
[BSD License](http://www.opensource.org/licenses/BSD-3-Clause)

Code and documents are copyright (C) 2009-20013, Jonathan Jacky.


Revised Apr 2013



