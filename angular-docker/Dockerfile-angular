### STAGE 1: Build ###
FROM node:14.15.2-alpine AS builder
WORKDIR /DockerAngularApp
COPY package.json package-lock.json ./
RUN npm i
COPY . .
RUN npm run build --prod

### STAGE 2: Run ###
FROM nginx:1.19.1-alpine
### COPY nginx.conf /etc/nginx/nginx.conf
COPY  --from=builder /DockerAngularApp/dist/docker-angular-app /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]