# Node image
FROM node:latest as build

# Working directory
WORKDIR /src

# Copy package.json and yarn.lock
COPY . .

# Install dependencies
RUN yarn global add http-server

# Copy the rest of the application code
COPY . .

# Run development build
CMD ["npx", "http-server", "-o", "--cors", "-a", "localhost", "-p", "8900"]