# build and unit tests

## Overview

![Build Stage](images/build.svg)

This stage contains the classic application build as well as any checks on the code in isolation (unit testing, static code analysis).

The goal of the test/checks in this stage is to make sure that each unit of code performs correctly. Buisness logic shoud - if possible - be checked in this stage.

## Steps

1. [code compilation and build](#code-compilation-and-build)
2. [unit tests](#unit-tests)
3. [static analysis](#static-analysis)
4. [dependency checks](#dependency-checks)
5. [security checks](#security-checks)
6. [artefact generation](#artefact-generation)

### code compilation and build

* build the code

Any build failure must stop the pipeline. This to provide fast feedback.

More details and tool suggestions: [build.md](build.md)

### unit tests

* run all unit tests
* collect test results
* collect test coverage

Failing unit tests will not stop the execution of the step.
This to collect the test results of all tests at the end of the step.
Any non passing test must change the status of this step to unstable.

Stop the pipeline if the step status returns unstable (failing unit tests).

Testing guidelines: [test pyramid](../../best-practices.md#testing)

### static analysis

Static code analysis (SCA) of the software source code.

* static code analysis
* Static Application Security Testing (SAST)

More details and tool suggestions: [static-analysis.md](static-analysis.md)

### dependency checks

* check dependencies for updates
* check dependencies for security problems
* license checks

More details and tool suggestions: [dependency-checks.md](dependency-checks.md)

### security checks

* Dynamic Application Security Testing (DAST)

More details and tool suggestions: [security-checks.md](security-checks.md)

### artefact generation

Packaging of the artefact.

## Stage Output

The output will be:

* application artifacts
* test results
