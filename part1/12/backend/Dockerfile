FROM node
ENV FRONT_URL=http://localhost:5000

WORKDIR /srv/app/
COPY ./backend-example-docker ./backend
WORKDIR /srv/app/backend
RUN npm install

EXPOSE 8000
CMD [ "npm", "start" ]
