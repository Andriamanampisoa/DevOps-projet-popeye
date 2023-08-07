FROM node:12-alpine

COPY . .

#Insralling requirements
RUN npm install

#Expose port
EXPOSE 80

CMD [ "node", "server.js" ]