#Stage 1
FROM node:21 as backend-builder

# Set the working directory inside the container
WORKDIR /app

# Copy the rest of the application code to the working directory
COPY . .

# Install required dependencies
RUN npm install

#stage 2
FROM node:21-slim
WORKDIR /app
COPY --from=backend-builder /app .

COPY .env.sample .env
# Expose the port the app runs on
EXPOSE 8000

# Command to start the backend server
CMD ["npm", "start"]
