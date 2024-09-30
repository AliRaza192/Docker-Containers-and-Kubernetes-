# Use the official node image for React
FROM node:lts

# Set the working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json /app/
RUN npm install

# Copy the rest of the application code
COPY . /app

# Expose port 3000
EXPOSE 3000

# Start the React application
CMD ["npm", "start"]
