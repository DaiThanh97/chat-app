FROM node:14-alpine AS build

RUN mkdir /backend
WORKDIR /backend

COPY package*.json ./ 

RUN npm install

COPY . .
RUN npm run build

#---------------------------

FROM node:14-alpine

RUN mkdir /backend
WORKDIR /backend

COPY package.json ./

RUN npm install --only=production

COPY . .

COPY --from=build /backend/dist ./dist

ENV NODE_ENV=production

CMD [ "npm", "start" ]