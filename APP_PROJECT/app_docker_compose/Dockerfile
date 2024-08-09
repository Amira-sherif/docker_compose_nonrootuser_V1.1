FROM python:3.9-slim

# Create a non-root user and group, and create a home directory
RUN groupadd -r amira && useradd -r -g amira -d /home/amira amira && mkdir -p /home/amira

# Verify the user was created (Optional debugging step)
RUN id amira

# Create the application directory
RUN mkdir /app

# Set ownership and permissions for the directories
RUN chown -R amira:amira /app /home/amira

# Set the working directory
WORKDIR /app

# Switch to the non-root user
USER amira

# Copy the application files
COPY . .

# Install dependencies without using the cache
RUN pip install --no-cache-dir -r req.txt

# Expose the application port
EXPOSE 5000

# Set the entrypoint for the container
ENTRYPOINT ["python", "app.py"]
FROM python:3.9-slim

# Create a non-root user and group, and create a home directory
RUN groupadd -r amira && useradd -r -g amira -d /home/amira amira && mkdir -p /home/amira

# Verify the user was created (Optional debugging step)
RUN id amira

# Create the application directory
RUN mkdir /app

# Set ownership and permissions for the directories
RUN chown -R amira:amira /app /home/amira

# Set the working directory
WORKDIR /app

# Switch to the non-root user
USER amira

# Copy the application files
COPY . .

# Install dependencies without using the cache
RUN pip install --no-cache-dir -r req.txt

# Expose the application port
EXPOSE 5000

# Set the entrypoint for the container
ENTRYPOINT ["python", "app.py"]
