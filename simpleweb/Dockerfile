# Specify a base image
FROM node:alpine

WORKDIR /usr/app

# Install some dependencies

# look in the current working directory
# aka the directory specified by the build context argument of Docker build, find the
# package.json file and then copy that into the current working directory of the container
# then run npm install

COPY ./package.json ./
RUN npm install
COPY ./ ./

# Default command
CMD ["npm", "start"]

