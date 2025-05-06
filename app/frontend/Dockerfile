# Use official Node.js Alpine image
FROM node:16.14-alpine

# Set working directory
WORKDIR /app-frontend

# Copy only package.json and package-lock.json first (layer caching for faster builds)
COPY package*.json ./

# Install dependencies
RUN npm install

# Then copy the rest of the code
COPY . .

# Build the project
RUN npm run build



# Start the app
CMD ["npm", "start"]

