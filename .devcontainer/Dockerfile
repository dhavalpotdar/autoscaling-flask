# Use the VS Code Python development container as the base image
ARG VARIANT="3.10-bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/python:0-${VARIANT}

# Copy the application files into the container
WORKDIR /app
COPY . /app

# Install necessary dependencies
RUN pip install --no-cache-dir Flask transformers

# Expose the port the app runs on
EXPOSE 5000

# Define environment variables
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

# Command to run the application
CMD ["flask", "run", "--host=0.0.0.0"]