FROM node
ENV API_URL=http://localhost:8000

WORKDIR /srv/app/
COPY ./frontend-example-docker ./frontend
WORKDIR /srv/app/frontend
RUN npm install

EXPOSE 5000
CMD [ "npm", "start" ]
