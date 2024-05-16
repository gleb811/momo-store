FROM node:16 as builder
WORKDIR /app
COPY ["package.json", "package-lock.json", "./"]
RUN npm install
COPY . .
RUN rm default.conf
RUN npm run build

FROM nginx:stable-alpine
COPY --from=builder /app/dist /usr/share/nginx/html
ADD /etc/nginx/ /etc/nginx/
RUN ls /etc/nginx/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
