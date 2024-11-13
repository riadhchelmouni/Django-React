# frontend/Dockerfile

# Use the Node.js image for building the React app
FROM node:18

# Set working directory
WORKDIR /app

# Install dependencies
COPY package.json .
RUN npm install

# Copy React project files
COPY . .

# Build the React app
RUN npm run build

# Serve the app on a static server
RUN npm install -g serve
CMD ["serve", "-s", "build"]

# Expose the port for the frontend
EXPOSE 3000
