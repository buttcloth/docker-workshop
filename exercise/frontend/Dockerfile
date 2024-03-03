FROM node:18

# Set the working directory inside the container to /exercise/frontend
WORKDIR /exercise/frontend

# Copy the package.json and package-lock.json to the working directory
COPY package*.json ./

# Run npm install to install the dependencies specified in package.json
# This is done before copying the rest of the application to utilize Docker's cache and avoid reinstalling all node_modules every build
RUN npm install

# Copy the rest of the application's source code
COPY . .

# Set an environment variable used by the application
ENV REACT_APP_BACKEND_URL=http://localhost:3000

# Build the application
RUN npm run build

# Command to start the app
CMD ["npm", "run", "start"]
