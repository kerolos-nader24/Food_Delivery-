# ===== Build Stage =====
FROM node:18-alpine AS builder
WORKDIR /app

# انسخ ملفات الباكج
COPY package*.json ./

# نصّب كل الحزم (بما فيها devDependencies)
RUN npm install

# انسخ باقي الكود
COPY . .

# ابني المشروع
RUN npm run build

# ===== Run Stage =====
FROM nginx:alpine
# Vite بيوصل build في dist/
COPY --from=builder /app/dist /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
