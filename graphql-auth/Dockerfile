
FROM node:20

WORKDIR /app

COPY package*.json ./

RUN npm install -g pnpm prisma

RUN pnpm install

COPY package.json pnpm-lock.yaml ./

COPY prisma ./prism

EXPOSE 8080

CMD  prisma migrate dev && pnpm run dev
