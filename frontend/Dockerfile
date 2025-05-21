FROM node:18-alpine

RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

WORKDIR /home/appuser/app

COPY . .

RUN npm install && npm run build && rm -rf /home/appuser/app/node_modules /home/appuser/.cache

CMD ["npx", "serve", "-s", "build"]
