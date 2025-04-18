# Use the official Node.js image with Alpine Linux for a minimal base image
FROM node:18-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json files from the wiki_watch subdirectory
COPY wiki_watch/package*.json ./wiki_watch/

# Install project dependencies
RUN npm install -g @angular/cli

# Copy the entire project directory to the container
COPY wiki_watch/ ./wiki_watch/

WORKDIR /app/wiki_watch
RUN npm install

# Expose the port the app runs on
EXPOSE 4200

# Start the Angular development server
CMD ["ng", "serve", "--host", "0.0.0.0"]