# Use an official Node.js image as the base image
FROM node:20

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the Next.js application
RUN npm run build

# Install PM2 globally if you want to use it (optional)
RUN npm install -g pm2

# Expose the port on which the app will run
EXPOSE 3000

# Use the command to start the app
# If using PM2:
CMD ["pm2-runtime", "npm", "--", "start"]
# Or without PM2:
# CMD ["npm", "start"]
