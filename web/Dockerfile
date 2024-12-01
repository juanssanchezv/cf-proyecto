# Stage 1: Build the application
FROM node:18 AS builder

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to install dependencies
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the application
RUN npm run build

# Exponer el puerto necesario y ejecutar la aplicación
EXPOSE 5173

# Iniciar la aplicación
CMD ["npm", "run", "dev"]
