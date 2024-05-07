FROM node:20

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY package*.json ./
RUN npm install
RUN npm install pm2 -g

# Bundle app source
COPY . .

EXPOSE 5000
CMD [ "pm2-runtime", "start", "server.js" ]

