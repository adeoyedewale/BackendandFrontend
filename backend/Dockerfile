# FROM node:14
FROM node:lts-alpine

# Set the working directory
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the application
#RUN npm run build

# Expose the port
EXPOSE 8080

# Build the application
#RUN npm build

# Start the application
# CMD ["npm", "ci" ]
# CMD [ "npm", "start" ]
CMD [ "node", "index.js" ]
