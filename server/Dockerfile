FROM node:18

WORKDIR /src

COPY . .

#command

RUN npm install
RUN npm install nodemon

EXPOSE 5000

CMD [ "npm", "start" ]