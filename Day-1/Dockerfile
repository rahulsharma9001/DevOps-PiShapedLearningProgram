# Use an official Python runtime as the base image
FROM python:3.11-slim

# Set the working directory
WORKDIR /app

# Copy the application code
COPY app.py /app

# Install Flask
RUN pip install flask

# Expose the port
EXPOSE 8080

# Run the app
CMD ["python", "app.py"]
