# Stage 1: Build the application
FROM node:22-slim as build
WORKDIR /order/src/app
COPY package*.json ./
RUN npm install
COPY . .

# Stage 2: Run the application
FROM node:22-slim
WORKDIR /order/src/app
COPY --from=build /order/src/app /order/src/app/
EXPOSE 3002
CMD ["node", "app.js"]
