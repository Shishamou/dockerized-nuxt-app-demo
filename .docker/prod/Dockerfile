FROM node:16-alpine AS build

WORKDIR /src

COPY package.json .

RUN yarn install \
  --prefer-offline \
  --frozen-lockfile \
  --non-interactive \
  --production=false

COPY . .
RUN npm run build --standalone \
  && npm run generate


FROM nginx:alpine AS runner

WORKDIR /usr/share/nginx/html

COPY --from=build /src/dist .

EXPOSE 80
