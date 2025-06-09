# Start from an official Ubuntu base image
FROM ubuntu:22.04

# Avoid prompts during installation
ARG DEBIAN_FRONTEND=noninteractive

# Update package list and install Apache2
RUN apt-get update && \
    apt-get install -y apache2 && \
    apt-get clean

# Copy your custom index.html (optional)
COPY index.html /var/www/html/index.html

# Expose port 80
EXPOSE 80

# Start Apache in the foreground
CMD ["apachectl", "-D", "FOREGROUND"]

