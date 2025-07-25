# Chiwawa Server - Стартовая страница
*Создатель: ebluffy*

## Описание проекта

Стартовая страница для приватного Minecraft сервера "Chiwawa Server" с системой подачи заявок.

### Возможности:
- 🎮 Стартовая страница с информацией о сервере
- 📝 Форма подачи заявки на вступление
- 🔍 Отображение статуса сервера (онлайн/оффлайн)
- 💬 Ссылка на Discord сервер
- 📱 Адаптивная верстка для мобильных устройств
- 🛡️ Валидация данных на frontend и backend
- 📋 Логирование заявок

## Установка и запуск

### 1. Установка зависимостей
```bash
cd backend
npm install
```

### 2. Запуск сервера
```bash
# Обычный запуск
npm start

# Или для разработки с автоперезагрузкой
npm run dev
```

### 3. Открытие сайта
Перейдите в браузере по адресу: http://localhost:3000

## Настройка

### Discord ссылка
В файле `website/script.js` измените строку:
```javascript
const DISCORD_INVITE = 'https://discord.gg/your-invite'; // Ваша ссылка
```

## Технологии

**Frontend:**
- HTML5, CSS3, JavaScript (ES6+)
- Адаптивная верстка (Flexbox, CSS Grid)
- Fetch API для HTTP запросов

**Backend:**
- Node.js + Express.js
- CORS middleware
- File-based logging
- JSON API