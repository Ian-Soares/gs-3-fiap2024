FROM node:22-alpine as build

WORKDIR /app

COPY package*.json ./

RUN npm install --production

COPY ./app.js ./

FROM node:22-alpine

RUN addgroup -S appgroup && adduser -S appuser -G appgroup

WORKDIR /app

COPY --from=build /app /app

USER appuser

EXPOSE 9090

CMD ["npm", "start"]
