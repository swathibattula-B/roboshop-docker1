 FROM node:20
  # this creates /app and move there
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install
ENV MONGO="true" \
    MONGO_URL="mongo://mongo:27017/catalogue" \
    REDIS_URL="redis://redis:6379"
CMD ["node", "server.js"]