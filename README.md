# Incorrect Usage of CMD in Dockerfile for Package Installation

This repository demonstrates a common error in Dockerfiles: using `CMD` to install packages. The provided `Dockerfile` incorrectly uses `CMD` to install the `requests` package using `pip`. This will only run the installation command once, the package won't be installed in subsequent uses of the image.

## Solution

The corrected `Dockerfile_fixed` shows how to properly install packages during the image build phase using `RUN`.