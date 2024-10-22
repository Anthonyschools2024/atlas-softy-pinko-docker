# Use the latest Ubuntu image
FROM ubuntu:latest

# Update and upgrade APT packages
RUN apt-get update && apt-get upgrade -y

# Command to output "Hello, World!"
CMD echo "Hello, World!"

# Use a base image that includes Python
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Install Python3, pip3, and Flask
RUN apt-get update && apt-get install -y python3 python3-pip && \
    pip3 install Flask

# Add this line to prevent the "EXTERNALLY-MANAGED" error
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Copy the Python script into the container
COPY api.py .

# Command to run the Flask app
CMD ["python3", "api.py"]
