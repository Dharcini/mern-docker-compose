FROM node:18.9.1

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 5050

CMD ["npm", "start"]

#If your backend uses dev tools to build (TypeScript, etc.), swap npm ci --only=production for npm ci and adjust the start command.

