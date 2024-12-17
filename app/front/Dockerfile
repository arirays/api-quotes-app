# Use Python 3.6 as the base image
FROM python:3.6

# Set the working directory inside the container to /app
WORKDIR /app

# Copy all files from the front service folder to /app
COPY . /app

# Install the required Python packages
RUN pip install -r requirements.txt

# Expose port 3001 for the front service
EXPOSE 3001

# Command to run front.py when the container starts
CMD ["python", "front.py"]

