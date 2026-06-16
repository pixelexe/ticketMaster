FROM node:24

WORKDIR /app

# Install dependencies
COPY frontend/package*.json ./
RUN npm ci

# Copy source
COPY frontend/ .

ENV HOST 0.0.0.0
EXPOSE 5173

CMD ["npm","run","dev","--","--host","0.0.0.0"]
