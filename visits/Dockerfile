FROM node:alpine

WORKDIR '/app'

# only try to rebuild the image any time that we change the package.json
# don't rebuild the image if we make any changes to the source code e.g index.js file
COPY package.json .
RUN npm install
COPY . .

CMD ["npm", "start"]