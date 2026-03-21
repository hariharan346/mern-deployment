# Use the official Node.js Alpine image (Alpine is a very small, lightweight Linux distribution)
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json BEFORE copying the rest of the code.
# This is a Docker Best Practice to cache installed modules if package.json hasn't changed.
COPY package*.json ./

# Install the Node.js dependencies
RUN npm install

# Copy all the remaining backend files into the container
COPY . .

# Expose port 5000 since your server.js runs on it
EXPOSE 5000

# The command to start the backend server
CMD ["npm", "start"]

