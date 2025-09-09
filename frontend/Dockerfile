# Используем официальный Node.js образ
FROM node:18-alpine

# Устанавливаем рабочую директорию
WORKDIR /app

# Копируем package.json и package-lock.json
COPY package*.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем исходный код
COPY . .

# Собираем приложение для продакшена
RUN npm run build

# Открываем порт 8000
EXPOSE 8000

# Запускаем встроенный веб-сервер разработки Node.js на порту 8000
CMD ["npx", "serve", "-s", "build", "-l", "8000"]


