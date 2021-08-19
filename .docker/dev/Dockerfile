FROM node:16-alpine

WORKDIR /app

COPY package.json .

RUN yarn install

ENV NUXT_HOST=0.0.0.0
ENV NUXT_PORT=3000
ENTRYPOINT [ "npm", "run", "dev" ]
EXPOSE 3000

