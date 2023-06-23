# Use an appropriate base image with Node.js pre-installed
FROM node:18

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install backend dependencies
RUN npm install

# Copy the rest of the backend code to the working directory
COPY . .

# Set environment variables if required
# ENV VAR_NAME=value

# Expose the port your backend server listens on (default: 5000)
EXPOSE 5000

# Start the backend server
CMD [ "npm", "start" ]