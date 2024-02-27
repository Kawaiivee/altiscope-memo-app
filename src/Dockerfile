# Node image
FROM node:latest as build

# Working directory
WORKDIR /s

# Copy package.json and yarn.lock
COPY . .

# Install dependencies
RUN yarn install

# Copy the rest of the application code
COPY . .

# Run development build
CMD ["npx", "http-server", "-o", "--cors", "-a", "127.0.0.1", "-p", "8900"]