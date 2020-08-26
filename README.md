# Algorithmic Testing

A simple package used in the testing of various algorithms.

The module is used in the Algorithmic Toolbox course in the Algorithms and Data Structures
Specialization course from Coursera.

The design pattern implemented here is the Strategy Pattern, which states the an algorithm
can be independant from the object and allows algorithms to be passed in to the object without
effecting the implementation of the system.

### The system consists of the following classes and sub-classes:

#### Algorithm

Base class of the algorithm. Defines the algorithm object.

#### AlgorithmTest

Abstract base class used as parent class for the two test classes.

#### AlgorithmTestMinimal

Inherits from AlgorithmTest class. This class specializes in running tests against
multiple algorithms with deterministic data points passed into the class at creation. The
algorithms are tested against each other. If the results differ the test fails

#### AlgorithmTestStress

Inherits from AlgorithmTest base class. The class specializes in running multiple algorithms
against stochastic data points for a predetermined amount of time. If the results of any of the
algorithms differs the test fails and results are printed.

#### TestResult

The class used to store the results from a single data point used in a test. The results
of each algorithm are passed to the test result. The class is used to check that all results
for each algorithm are the same for a given data point.
