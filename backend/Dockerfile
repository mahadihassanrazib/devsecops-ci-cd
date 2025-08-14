# Stage 1: Build the Node.js backend app
FROM node:18-alpine3.20 AS build

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json (if available) to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the container
COPY . .

# Expose the port where your app will run (default: 3000)
EXPOSE 3000

# Command to start the Node.js server
CMD ["npm", "start"]