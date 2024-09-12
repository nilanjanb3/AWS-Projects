# This Dockerfile builds an image for a web application using nginx
# It uses the latest available version of nginx on the amd64 platform
FROM --platform=linux/amd64 nginx:latest

# Set the working directory to /usr/share/nginx/html
WORKDIR /usr/share/nginx/html

# Copy the index.html file from the current directory into the container
# The file will be named index.html in the container
COPY index.html index.html
