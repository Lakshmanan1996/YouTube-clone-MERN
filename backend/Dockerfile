FROM node:20-alpine

WORKDIR /app/backend

# Copy only package files first (layer caching)
COPY package*.json ./

RUN npm install --only=production

# Copy app source
COPY . .

EXPOSE 5000

CMD ["node", "server.js"]
