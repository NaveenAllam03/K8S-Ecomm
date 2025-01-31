# FROM node:18.9.1-alpine3.19
# EXPOSE 8080
# RUN addgroup -S roboshop && adduser -S roboshop -G roboshop 
# WORKDIR /opt/server
# COPY package.json /opt/server/
# COPY server.js /opt/server/
# RUN npm install 
# CMD ["node", "server.js"]

FROM nginx
RUN rm -rf /usr/share/nginx/html/index.html 
RUN rm -rf /usr/nginx/nginx.conf
RUN rm -rf /usr/nginx/conf.d/default.conf
COPY  roboshop.conf /etc/nginx/nginx.conf
ADD static /usr/share/nginx/html