# Create image based on the official Node 10 image from dockerhub
FROM node:latest

# Create a directory where our app will be placed
RUN mkdir -p /app

# Change directory so that our commands run inside this new directory
WORKDIR /app

# Copy dependency definitions
COPY package*.json /app/

# Install dependecies
RUN npm install

# Get all the code needed to run the app
COPY . /app/

#ENV APIURL=<backend-app-service-ip>:<port>

#ENV API_KEY=192.168.64.3:31734


# Expose the port the app runs in
EXPOSE 4200
#EXPOSE 80

# Serve the app
CMD ["npm", "start"]


#
#
##+++++++++++++++++++++++++++++++
##NEED FOR RUNNING IN MINIKUBE
##++++++++++++++++++++++++++++++++
## Create image based on the official Node 10 image from dockerhub
#FROM node:latest
## Create a directory where our app will be placed
#RUN mkdir -p /app
## Change directory so that our commands run inside this new directory
#WORKDIR /app
## Copy dependency definitions
#COPY package*.json /app/
## Install dependecies
#RUN npm install
## Get all the code needed to run the app
#COPY src /app/src/
#COPY public /app/public/
#COPY env.sh /app/
##COPY build env.js env.js.sh ./
#RUN pwd
#RUN ls
#RUN chmod +x env.sh
## Expose the port the app runs in
#EXPOSE 3000
## Serve the app
#CMD ./env.sh "$API_KEY" && npm start
#
