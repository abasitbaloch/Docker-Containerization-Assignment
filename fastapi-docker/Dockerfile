# Install python version 3.12
FROM python:3.12-slim 

# Set working directory
WORKDIR /app 

# Copy all files
COPY . . 

# Install uv using pip
RUN pip install uv 

# Install all dependencies
RUN uv sync 

# Application access port
EXPOSE 8000 

# Run the application
CMD ["uv", "run", "fastapi", "dev", "main.py", "--host", "0.0.0.0"]