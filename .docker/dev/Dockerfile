FROM node:16-alpine

WORKDIR /app

COPY package.json .
RUN yarn

COPY . .

ENV NUXT_HOST=0.0.0.0
ENTRYPOINT [ "npm", "run", "dev" ]

