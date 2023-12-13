FROM node:17.0-alpine3.14
ENV APP_HOME=/app
RUN mkdir -p $APP_HOME
RUN mkdir -p $APP_HOME/views
WORKDIR $APP_HOME
COPY package*.json .
RUN apk add npm=7.17.0-r0 && npm install
COPY app.js .
COPY ["index.pug", "favicon.ico", "./views/"]
EXPOSE 80
CMD ["node", "app.js"]
