# Use an official GCC base image
FROM gcc:latest

# Set the working directory inside the container
WORKDIR /app

# Copy the source code into the container
COPY main.cpp .

# Compile the C++ program
RUN g++ -o hello main.cpp

# Define the command to run the compiled program
CMD ["./hello"]
