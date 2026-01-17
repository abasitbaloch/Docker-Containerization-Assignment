# Install nodejs version 22
FROM node:22-alpine 

# Set working directory
WORKDIR /app 

# Copy package files
COPY package*.json ./ 

# Install dependencies
RUN npm install

# Copy all files
COPY . . 

# Build the project
RUN npm run build

# Application access port
EXPOSE 3000 

# Run the application
CMD ["npm", "start"]