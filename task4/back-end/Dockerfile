# Use the latest Ubuntu image as base
FROM ubuntu:latest

# Update APT and upgrade installed software
RUN apt-get update && apt-get upgrade -y

# Install Python3, pip3, and Flask dependencies
RUN apt-get install -y python3 python3-pip

# Remove the "EXTERNALLY-MANAGED" file to avoid issues with pip3
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask and Flask-CORS
RUN pip3 install flask flask-cors

# Set the working directory
WORKDIR /app

# Copy the local api.py file to the container
COPY api.py /app/api.py

# Expose port 5252 for Flask server
EXPOSE 5252

# Command to run the Flask server
CMD ["python3", "api.py"]
