# Dockerfile
FROM node:18-alpine

WORKDIR /usr/app

COPY package*.json ./
RUN npm install

COPY . .

# Install TypeScript and build the project
RUN npm install -g typescript
RUN npm run build

# Expose the application port
EXPOSE 3000

CMD ["node","server.ts"]