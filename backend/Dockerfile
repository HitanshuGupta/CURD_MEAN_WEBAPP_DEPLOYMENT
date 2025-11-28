# Base Image
FROM node:18-alpine

# Working Directory
WORKDIR /app

# Copy Package Files
COPY package*.json ./

# Install Dependencies
RUN npm install

# Copy Source Code
COPY . .

# Expose the API Port
EXPOSE 8080

# Start Command
CMD ["npm", "start"]