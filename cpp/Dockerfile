FROM gcc:latest

# Install CMake and make
RUN apt-get update && apt-get install -y cmake make

# Copy everything into the container
COPY . /usr/src/mytest

RUN ls -la /usr/src/mytest


# Set the working directory
WORKDIR /usr/src/mytest

# Create build directory
RUN mkdir build

# Move into the build directory
WORKDIR /usr/src/mytest/build

# Run CMake and Make
RUN cmake .. && make

# Run the tests when the container starts
CMD ["./runTests"]
