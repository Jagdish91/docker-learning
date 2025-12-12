# Declares the base image for you your build, pulls the specified version of Ubuntu from Docker Hub if not available locally
# Base image determines the OS, package manager,system libaries, shell and initial filesystem layout
# It's the first layer, all subsequent additions/changes are layered on the top
FROM ubuntu:3.11-slim

# Sets the working directory subsequent instructions (COPY, RUN) and for the container at runtime
# if /app doesn't exits, Docker creates it. cleaner than (RUN mkdir /app && cd /app )
WORKDIR /app

# Copy files from the build context (the directory you run docker build from) into the image at /app (here copy python file)
COPY . /app

# Run shell during image build time and executes teh commands.
RUN apt-get update && apt-get install -y --no-install-recommends python3 python-pip

# Set environmental variables
ENV NAME World

# Run a command to start the application
CMD ["python3", "app.py"]








