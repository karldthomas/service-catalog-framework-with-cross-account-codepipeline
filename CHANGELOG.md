#CHANGELOG

## Version 1.1

### New Features

- CodeBuild role is no longer hard coded and can be specified when launching the product
- The CodeBuild image is configurable between v4.0 and v5.0
- Resource names are no longer created based on the branch.  The branch can have characters that are not allowed resource names.
- upgraded Lambdas from Python 3.7 to Python 3.9

### Fixes

- Corrected Python version specified in the buildspec files
