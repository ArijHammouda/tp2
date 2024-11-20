# Use node:lts-alpine as the base image
FROM node:lts-alpine

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package*.json files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the client files
COPY . .

# Build the React app
RUN npm run build

# Install a lightweight HTTP server to serve the build
RUN npm install -g serve

# Expose port 3000
EXPOSE 3000

# Serve the React app
CMD ["serve", "-s", "build"]
