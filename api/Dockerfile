FROM node:alpine

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install

# Bundle app source
COPY . .

RUN npm run build
# Bind your app to port 8080
EXPOSE 8000

# CMD [ "node", "server.js" ]
CMD [ "node", "dist/index.js" ]