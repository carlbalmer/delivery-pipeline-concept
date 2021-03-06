# manual tests

This stage is used to test borderline cases which can not accomplished with automated tests.

## Overview

![Manual Tests Stage](images/manual-tests.svg)

## Steps

1. deployment to [uat](https://en.wikipedia.org/wiki/Acceptance_testing) test environment
2. automated smoke tests
3. manual tests

## Stage Output

Passing this step means that the deployable artefact from the [packaging stage](../02-packaging/README.md) is ready to deployed to production.

The output will be:

* test report
