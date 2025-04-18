# Use the official Node.js image as the base image
FROM node:18

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory to install dependencies
COPY package*.json ./

# Install application dependencies
RUN npm install --production

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port that the Fastify application listens on
EXPOSE 3000

# Define the command to run the application
CMD ["node", "server.js"]