FROM node:boron

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Install app dependencies
COPY web3.js/* /usr/src/app/
#RUN npm install

EXPOSE 8080
CMD [ "npm", "start" ]
