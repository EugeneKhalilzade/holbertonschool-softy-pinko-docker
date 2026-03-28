# Base image
FROM ubuntu:latest

# Update & upgrade
RUN apt-get update && apt-get upgrade -y

# Install python + pip
RUN apt-get install -y python3 python3-pip

# Fix externally managed error (IMPORTANT)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask with pip3
RUN pip3 install flask
RUN pip3 install flask-cors

# Set working directory
WORKDIR /app

# Copy app file
COPY ./api.py /app/api.py

# Run the app
CMD ["python3", "api.py"]
