# Use an appropriate base image for your frontend (e.g., Node.js with React pre-installed)
FROM node:18

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install frontend dependencies
RUN npm install

# Copy the rest of the frontend code to the working directory
COPY . .

# Set environment variables if required
# ENV VAR_NAME=value

# Build the frontend code
RUN npm run build

# Serve the built frontend code using a lightweight web server (e.g., serve)
RUN npm install -g serve

# Expose the port your frontend app listens on (default: 3000)
EXPOSE 3000

# Start the web server to serve the built frontend
CMD [ "serve", "-s", "build" ]
