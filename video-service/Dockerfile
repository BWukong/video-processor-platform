# parent node image from Docker
FROM node:20

# Set working directory in container to /app
WORKDIR /app

# copy packages into container
COPY package*.json ./

# install ffmpeg
RUN apt-get update && apt-get install -y ffmpeg

# Install node modules
RUN npm install

COPY . .

# make port 3000 available
EXPOSE 3000

# command to start running the application
CMD [ "npm", "start" ]