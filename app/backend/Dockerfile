# Use lightweight Node.js image
FROM node:16.14-alpine

# Set working directory inside container
WORKDIR /app-backend

# Copy only dependency files first for better caching
COPY package*.json ./

# Install only production dependencies if it's a production app
RUN npm install --production

# Copy the rest of the backend code
COPY . .


# Start the backend server
CMD ["npm", "start"]

