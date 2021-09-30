FROM node:alpine

ENV DB_CONNECTION=mysql
ENV DB_HOST=app_db
ENV DB_PORT=3306
ENV DB_DATABASE=userdb
ENV DB_USERNAME=app_user
ENV DB_PASSWORD=userpass

WORKDIR /app

COPY package*.json ./

RUN yarn install

COPY . .

RUN yarn build

EXPOSE 8080
CMD [ "yarn", "start:prod" ]
