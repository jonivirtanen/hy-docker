FROM node

WORKDIR /srv/app/
COPY ./frontend-example-docker ./frontend
WORKDIR /srv/app/frontend
RUN npm install

EXPOSE 5000
CMD [ "npm", "start" ]
