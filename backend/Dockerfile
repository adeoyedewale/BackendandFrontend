# FROM node:14
FROM node:lts-alpine

# Create a directory for the app
RUN mkdir -p /usr/src/backend

# Set the working directory
WORKDIR /usr/src/backend

# Copy the package.json and package-lock.json
COPY backend/package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY backend/. .

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
