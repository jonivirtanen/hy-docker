#nodejs-dev-env

FROM node:12-stretch
EXPOSE 3000

RUN npm install -g nodemon

WORKDIR /src/

CMD [ "nodemon", "./index.js" ]
