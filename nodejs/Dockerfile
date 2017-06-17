FROM node:boron

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Ensure DNS configuration
RUN echo -e "nameserver 8.8.8.8\nnameserver 8.8.4.4" > /etc/resolv.conf

# Install app dependencies
COPY web3.js/* /usr/src/app/
RUN npm install

EXPOSE 8080
CMD [ "npm", "start" ]
