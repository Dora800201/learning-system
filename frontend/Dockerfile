# Use a Node.js base image
FROM node:18

# Set working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci

# Build the React app for production
COPY . .
RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
