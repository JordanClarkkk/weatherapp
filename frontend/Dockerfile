FROM node:16.4.0

WORKDIR /frontend

COPY package*.json ./

RUN npm install 

COPY . .

ENV PORT=8081

EXPOSE 8081

CMD ["npm", "start"]