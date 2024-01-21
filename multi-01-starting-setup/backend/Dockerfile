FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

# ENV MONGODB_USERNAME='root'
# ENV MONGODB_PASSWORD='admin@123'

CMD [ "node", "app.js" ]