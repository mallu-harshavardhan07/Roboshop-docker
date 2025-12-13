FROM node:20
WORKDIR /opt/server
COPY package.json .
COPY server.js .
ENV REDIS_URL='redis://redis:6379' \
    MONGO_URL="mongodb://mongodb:27017/users"
CMD ["node", "server.js"]