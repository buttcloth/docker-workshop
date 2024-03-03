FROM node:18

# Sets the working directory inside the container to /exercise/backend
WORKDIR /exercise/backend

# Copy the package.json and package-lock.json to the working directory
COPY package*.json ./

# Run npm install to install the dependencies specified in package.json
# This is done before copying the rest of the application to utilize Docker's cache and avoid reinstalling all node_modules every build
RUN npm install

# Copy the rest of the application's source code into the container
COPY . .

# Sets the port for backend to run on with PORT environment variable
ENV PORT=3000

# Command to start the app
CMD ["node", "index.js"]
