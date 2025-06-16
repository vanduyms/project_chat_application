FROM node:18 AS build

WORKDIR /src

COPY . .

ENV NODE_OPTIONS=--openssl-legacy-provider

RUN npm install
RUN npm run build

FROM nginx:alpine
COPY --from=build /src/build /usr/share/nginx/html

EXPOSE 80
CMD [ "nginx", "-g", "daemon off;" ]