FROM node:14.16.0-alpine3.13
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . . 

EXPOSE 3001

# RUN ["chmod", "+x", "/app/docker-entrypoint.sh"]
# RUN ["chmod", "+x", "/app/wait-for"]
RUN npm run db:up

CMD ["npm", "start"]