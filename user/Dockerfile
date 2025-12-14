FROM node:20

# Set working directory
WORKDIR /opt/server

# Copy package.json and package-lock.json (if exists) first
COPY package*.json ./

# Install all Node.js dependencies
RUN npm install

# Copy the rest of the application
COPY server.js .  

# Set environment variables
ENV REDIS_URL='redis://redis:6379' \
    MONGO_URL='mongodb://mongodb:27017/users'

# Expose the port the app listens on
EXPOSE 8080

# Start the Node.js application
CMD ["node", "server.js"]
