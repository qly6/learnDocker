FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV MONGODB_USERNAME=''
ENV MONGODB_PASSWORD=''

CMD [ "node", "app.js" ]