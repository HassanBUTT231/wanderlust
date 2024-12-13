FROM node:21
WORKDIR /app
COPY . .
# Copy the .env.sample file to .env.local
COPY .env.sample .env.local

# Expose port 5173 for the Node.js application
EXPOSE 5173

# Define the default command to run the application in development mode
CMD ["npm", "run", "dev", "--", "--host"]
