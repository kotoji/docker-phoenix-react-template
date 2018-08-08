FROM node:8.11.3

WORKDIR /app

RUN npm init -y
COPY ./package.json /app/package.json
RUN npm install
COPY ./webpack.config.js /app/webpack.config.js
COPY ./tsconfig.json /app/tsconfig.json

EXPOSE 8080

CMD ["npm", "start"]
