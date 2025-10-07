# Use official Node.js 20 image with Python installed
FROM node:20-bullseye

# Install Python 3 and pip
RUN apt-get update && apt-get install -y python3 python3-pip

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install Node.js dependencies
RUN npm install

# Copy backend source code
COPY . .

# Install Python dependencies
RUN pip3 install --no-cache-dir -r requirements.txt

# Expose backend port (5000 or as per your server.js)
EXPOSE 5000

# Start your Node.js server
CMD ["node", "server.js"]
