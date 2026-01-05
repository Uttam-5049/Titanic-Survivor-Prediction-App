FROM node:14

WORKDIR /frontend

# Copy package files
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy application files
COPY . .

# Set the API URL as a build argument
ARG REACT_APP_API_URL=http://localhost:8001
ENV REACT_APP_API_URL=$REACT_APP_API_URL

# Expose port
EXPOSE 3000

# Start the application
CMD ["npm", "start"]