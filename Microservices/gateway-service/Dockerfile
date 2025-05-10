# Stage 1: Build the application
FROM node:22-slim as build
WORKDIR /gateway/src/app
COPY package*.json ./
RUN npm install
COPY . .

# Stage 2: Run the application
FROM node:22-slim
WORKDIR /gateway/src/app
COPY --from=build /gateway/src/app /gateway/src/app/
EXPOSE 3003
CMD ["node", "app.js"]
