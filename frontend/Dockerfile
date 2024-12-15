FROM node:21 as frontend-builder
WORKDIR /app
COPY package*.json ./
RUN npm i
COPY . .
#stage 2
FROM node:21-slim
WORKDIR /app
COPY --from=frontend-builder /app .
COPY .env.sample .env.local

EXPOSE 5000

CMD ["npm","run","dev", "--","--host"]
~
