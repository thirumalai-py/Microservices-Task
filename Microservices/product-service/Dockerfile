# Stage 1: Build the application
FROM node:22-slim as build
WORKDIR /product/src/app
COPY package*.json ./
RUN npm install
COPY . .

# Stage 2: Run the application
FROM node:22-slim
WORKDIR /product/src/app
COPY --from=build /product/src/app /product/src/app/
EXPOSE 3001
CMD ["node", "app.js"]
