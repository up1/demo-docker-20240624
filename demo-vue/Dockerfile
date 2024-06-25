FROM node:22 as step01
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build

FROM nginx:1.27.0
COPY --from=step01 /app/dist /usr/share/nginx/html