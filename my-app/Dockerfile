Use an official Node.js runtime as a parent image
FROM node:22

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./


# Copy the rest of the application code
COPY . .

# Install dependencies
RUN npm install


# Build the React app
RUN npm run build

# Expose port for the application
EXPOSE 3000

# Set the command to run when the container starts
CMD ["npx", "serve", "-s", "build"]
