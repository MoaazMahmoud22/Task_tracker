FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci            # not npm install → reproducible
COPY . .
EXPOSE 3005
CMD ["npm","start"]
