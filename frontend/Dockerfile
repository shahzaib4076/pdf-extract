# Stage 1: Build the Angular app
FROM node:20-alpine AS build-stage

WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the application code
COPY . .

# Accept the API URL as a build argument (required by @ngx-env/builder)
ARG NG_APP_API_URL=http://localhost:8000/api
ENV NG_APP_API_URL=$NG_APP_API_URL

# Build the app to the dist folder
RUN npm run build

# Stage 2: Serve the app using Nginx
FROM nginx:stable-alpine

# Copy the built files from the build stage
COPY --from=build-stage /app/dist/pdf-extract/browser /usr/share/nginx/html

# Copy the Nginx config for Angular HTML5 routing support
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Expose port 80
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
