# ---------- مرحلة ❶: بناء تطبيق React -----------------
FROM node:20-alpine AS builder

# 1) مجلد العمل داخل الصورة
WORKDIR /app

# 2) تثبيت الاعتماديات بدون تحمّل node_modules إلى الـ Layer النهائي
COPY package*.json ./
RUN npm ci

# 3) نقل بقية الكود وبناء نسخة الإنتاج
COPY . .
#  -- المتغير يُمَرّر من docker-compose (args)
ARG REACT_APP_API_URL
ENV REACT_APP_API_URL=$REACT_APP_API_URL
RUN npm run build              # يضع الملفات في /app/build

# ---------- مرحلة ❷: تشغيل Nginx لخدمة الملفات ----------
FROM nginx:1.25-alpine

# 4) نسخ ملفات البناء إلى المسار الافتراضي لـ Nginx
COPY --from=builder /app/build /usr/share/nginx/html

# 5) ملف إعداد Nginx مُخصص يمرِّر /api إلى حاوية backend
COPY nginx.conf /etc/nginx/conf.d/default.conf

# 6) فتح المنفذ 80 داخل الحاوية (سنربطه بـ 3000 على المضيف)
EXPOSE 80

# 7) تشغيل Nginx في الـ Foreground
CMD ["nginx","-g","daemon off;"]
