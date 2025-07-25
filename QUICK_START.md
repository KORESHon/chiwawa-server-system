# 🎮 Chiwawa Server - Быстрый старт
*Создатель: ebluffy*

## Что создано:

### ✅ Frontend (website/)
- **index.html** - Главная страница с логотипом "Chiwawa Server"
- **styles.css** - Адаптивная верстка для всех устройств 
- **script.js** - JavaScript для формы заявок и API

### ✅ Backend (backend/)
- **server.js** - Express сервер с API endpoints
- **package.json** - Конфигурация Node.js проекта

## 🚀 Как запустить:

### Способ 1: Автоматический (Windows)
Дважды кликните на файл `start.bat` в корне проекта

### Способ 2: Ручной
```bash
cd backend
npm install
node server.js
```

## 🌐 Использование:

1. Откройте браузер и перейдите на http://localhost:3000
2. Увидите стартовую страницу Chiwawa Server
3. Нажмите "Подать заявку" для тестирования формы
4. Заполните форму и отправьте заявку
5. Заявка сохранится в `backend/applications.log`

## 🔧 API для тестирования:

### Проверка статуса сервера:
```bash
curl http://localhost:3000/api/status
```

### Отправка заявки:
```bash
curl -X POST http://localhost:3000/api/apply \
  -H "Content-Type: application/json" \
  -d '{
    "minecraft_nick": "TestPlayer",
    "discord": "test#1234", 
    "email": "test@example.com",
    "reason": "Хочу поиграть на вашем сервере"
  }'
```

### Просмотр заявок:
```bash
curl http://localhost:3000/api/applications
```

## 📱 Возможности:

- ✅ Адаптивная верстка (работает на мобильных)
- ✅ Модальное окно для подачи заявки  
- ✅ Валидация форм на frontend и backend
- ✅ Автоматическое логирование заявок
- ✅ Статус сервера (пока заглушка)
- ✅ Ссылка на Discord (настраивается в script.js)
- ✅ Обработка ошибок и уведомления пользователю

## 🎯 Что нужно настроить:

1. **Discord ссылка**: В `website/script.js` замените:
   ```javascript
   const DISCORD_INVITE = 'https://discord.gg/your-invite';
   ```

2. **Email контакт**: В `website/index.html` замените:
   ```html
   <a href="mailto:admin@chiwawa.site">admin@chiwawa.site</a>
   ```

## 🔍 Тестирование:

1. Проверьте отправку заявки через форму
2. Убедитесь что заявка появилась в `backend/applications.log`
3. Проверьте адаптивность на мобильном (F12 → Device Toolbar)
4. Протестируйте валидацию (пустые поля, неверный email)

---

**Проект полностью готов к использованию!** 🎉

Все требования из ТЗ выполнены:
- ✅ Стартовая страница с логотипом и описанием
- ✅ Кнопки "Подать заявку" и "Discord"  
- ✅ Форма заявки с нужными полями
- ✅ Backend с валидацией и логированием
- ✅ API endpoints POST /api/apply и GET /api/status
- ✅ Адаптивная верстка
- ✅ Обработка ошибок
- ✅ Все комментарии "Создатель: ebluffy"
