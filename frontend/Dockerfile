# Stage 1: Build Angular App
FROM node:18-alpine as build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
# Build command
RUN npm run build --prod

# Stage 2: Serve with Nginx
FROM nginx:alpine

COPY --from=build /app/dist/angular-15-crud /usr/share/nginx/html

# Expose internal port
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]