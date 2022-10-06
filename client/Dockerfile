#FROM node:lts-alpine
#ENV NODE_ENV=production
#WORKDIR /usr/src/app
#COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
#RUN npm install --production  && mv node_modules ../
#COPY . .
#EXPOSE 4000
#RUN chown -R node /usr/src/app
#USER node
#CMD ["npm", "start"]
FROM node:lts-alpine
WORKDIR /client
COPY package*.json /client/
RUN npm install
COPY . /client/
EXPOSE 3000
CMD [ "npm", "start"]