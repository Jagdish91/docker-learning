FROM node:25-alpine

# Create a app directory and set it to default directory and exuceute all the following commands from here
WORKDIR /usr/app

# Copy package.json , wildcard means also copy package-lock.json to the working directory
COPY package*.json ./

# Copy files from src directory
COPY src ./

# Install app dependencies
RUN npm install 

# Start the application
CMD ["node", "server-js"]
