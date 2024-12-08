FROM node:20.18.0-alpine3.20
EXPOSE 8080
ENV "DB_HOST"="mysql"
RUN addgroup -S expense && adduser -S expense -G expense && \
     mkdir /opt/server/ && \
     chown -R expense:expense /opt/server
WORKDIR /opt/server/
COPY package.json . && \
     *.js .
RUN npm install
USER expense
EXPOSE 8081
RUN echo "Hello World"
RUN echo "Hello Docker"
CMD ["node","index.js"]


#Before best practices implemented 

# FROM node:20
# EXPOSE 8080
# ENV "DB_HOST"="mysql"
# RUN mkdir /opt/server/
# WORKDIR /opt/server/
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD ["node","index.js"]