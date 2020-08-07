# build stage
FROM node:10-alpine as builder
WORKDIR '/app'
# copy package.json into the current working directory 
# e.g. into /app
COPY package.json . 
RUN npm install
COPY . .
RUN npm run build

# run stage
# To specify the start of a second phase all we 
# have to do is say FROM and then the name of our base
# image which is nginx
FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html
# the default command of nginx will start up the nginx server
