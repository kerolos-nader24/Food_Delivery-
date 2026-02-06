# نستخدم نسخة خفيفة من Node
FROM node:20-alpine

# نحدد مكان العمل جوه الكونتينر
WORKDIR /app

# ننقل ملفات الـ package.json عشان نعمل npm install
COPY package*.json ./

# تنصيب الحزم
RUN npm install

# ننقل باقي الملفات
COPY . .

# نفتح البورت اللي السيرفر هيشتغل عليه
EXPOSE 4000

# أمر تشغيل السيرفر
CMD ["node", "server.js"]
