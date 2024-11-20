# Use node:lts-alpine as the base image
FROM node:lts-alpine

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package*.json files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the server files
COPY . .

# Expose port 9000
EXPOSE 9000

# Set environment variables (you can set MONGO_URI in docker-compose)
ENV MONGO_URI=mongodb://mongodb:27017/mern

# Run the app
CMD ["npm", "start"]
