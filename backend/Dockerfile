#Use lightweight Node image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package files first (for caching)
COPY package*.json ./

# Install only production dependencies
RUN npm install --only=production

# Copy rest of the code
COPY . .

# Expose backend port (match your env → 8080)
EXPOSE 8080

# Start the app
CMD ["npm", "start"]
