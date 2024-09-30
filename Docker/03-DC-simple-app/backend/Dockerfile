# Base image
FROM node:lts

# Set the working directory inside the container
WORKDIR /code

# Copy package.json and package-lock.json to the container
COPY package.json /code/package.json
COPY package-lock.json /code/package-lock.json

# Install dependencies
RUN npm ci

# Copy the rest of the application code to the container
COPY . /code

# Expose the port the app will run on
EXPOSE 3000

# Set environment variables (optional)
ENV NODE_ENV=production

# Default command to run your app
CMD ["node", "src/index.js"]
