# Stage 1: Build the application
FROM node:22-slim as build
WORKDIR /user/src/app
COPY package*.json ./
RUN npm install
COPY . .

# Stage 2: Run the application
FROM node:22-slim
WORKDIR /user/src/app
COPY --from=build /user/src/app /user/src/app/
EXPOSE 3000
CMD ["node", "app.js"]
