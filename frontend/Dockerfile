FROM node:24

WORKDIR /app

# Install dependencies
COPY frontend/package*.json ./
# Use `npm install` to avoid failing on lockfile/package.json mismatches in CI
# and allow installing despite peer-dep conflicts during development builds.
RUN npm install --legacy-peer-deps

# Copy source
COPY frontend/ .

ENV HOST 0.0.0.0
EXPOSE 5173

CMD ["npm","run","dev","--","--host","0.0.0.0"]
