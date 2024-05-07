# Use the official Node.js 20 image as a parent image
FROM node:20-alpine

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (or yarn.lock if present)
COPY package*.json yarn.lock* ./

# Install dependencies
RUN npm install

# Copy the rest of your app's source code from your host to your image filesystem.
VOLUME [ "/usr/src/app" ]

# Inform Docker that the container listens on port 3000 at runtime.
EXPOSE 3000

# Use CMD instead of ENTRYPOINT to allow overriding the command, facilitating hot reloading
CMD ["npm", "run", "dev"]
