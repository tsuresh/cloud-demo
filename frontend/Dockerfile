# Use the official Node.js 19 image as the base image
FROM node:19

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN yarn install

# Copy the rest of the application code to the working directory
COPY . .

# Build the Next.js app
RUN yarn build

# Expose the port that the app will run on
EXPOSE 3000

# Start the app
CMD ["yarn", "start"]