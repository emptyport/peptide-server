FROM node:20-alpine

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY package*.json ./
RUN npm install
RUN npm install pm2 -g

# Mount the app source for hot reloading
VOLUME [ "/usr/src/app" ]

EXPOSE 5000
CMD [ "pm2-runtime", "start", "ecosystem.config.js" ]
