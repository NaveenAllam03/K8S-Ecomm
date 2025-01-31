FROM node:18
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop 
WORKDIR /opt/server
# ENV MONGO= true --> This environment we pass it from the Kubernetes as ConfigMap.
# giving ownership to user <user:owner>
RUN chowm roboshop:roboshop /opt/server 
USER roboshop
COPY package.json /opt/server/
COPY server.js /opt/server/
RUN npm install 
CMD ["node", "server.js"]