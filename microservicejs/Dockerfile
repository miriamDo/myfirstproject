# Base image
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json files
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

ARG CACHEBUST=1
# Build the React app
RUN npm run build

# Expose the container's port (adjust as per your application)
EXPOSE 3000

# Start the microservice
CMD ["npm", "start"]


