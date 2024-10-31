# Use the latest Ubuntu image
FROM ubuntu:latest

# Update and upgrade APT packages
RUN apt-get update && apt-get upgrade -y

# Set the working directory in the container
WORKDIR /app

# Install Python3, pip3, and Flask
RUN apt-get update && apt-get install -y python3 python3-pip

RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip3 install flask flask-cors

# Copy the Python script into the container
COPY api.py .

# Command to run the Flask app
CMD ["python3", "api.py"]
