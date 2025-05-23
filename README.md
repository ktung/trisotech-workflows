# Trisotech workflows

## Remove tests workflow
The remove-tests workflow removes the test cases section from a DMN file. This file should be smaller than the original file to speed up the deployment.

### Example
```yml
name: Remove Tests

on:
  workflow_dispatch:
  pull_request:

jobs:
  remove_tests:
    uses: ktung/trisotech-workflows/.github/workflows/remove-tests.yml@main
    with:
      src: example.dmn
      dst: example-notests.dmn
```

### Permissions
The remove-tests workflow requires the write contents permissions in order to write the destination file.
