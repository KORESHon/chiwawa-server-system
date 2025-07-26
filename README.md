# Chiwawa Server - Приватный Minecraft сервер

<div align="center">
  <h2>🐕 Добро пожаловать на сервер Chiwawa! 🐕</h2>
  <p><em>Приватный Minecraft сервер с дружелюбным сообществом</em></p>
</div>

## 📋 Описание проекта

Chiwawa Server - это веб-сайт для приватного Minecraft сервера с полнофункциональной системой пользователей. Проект включает в себя регистрацию, авторизацию, профили пользователей, админ-панель и систему заявок на присоединение к серверу.

## ✨ Основные возможности

- 🔐 **Система авторизации** - Безопасная регистрация и вход
- 👤 **Профили пользователей** - Персональные страницы с информацией об игроке
- 📝 **Система заявок** - Подача заявок на присоединение к серверу
- 🛡️ **Админ-панель** - Управление пользователями и заявками
- 📧 **Восстановление пароля** - Безопасное восстановление доступа
- 🎨 **Современный дизайн** - Minecraft-стилизованный интерфейс
- 📱 **Адаптивность** - Поддержка всех устройств

## 🚀 Технологии

### Backend
- **Node.js** - Серверная платформа
- **Express.js** - Веб-фреймворк
- **PostgreSQL** - База данных
- **JWT** - Аутентификация
- **bcryptjs** - Хеширование паролей
- **Helmet** - Безопасность
- **CORS** - Кросс-доменные запросы

### Frontend
- **HTML5/CSS3** - Разметка и стили
- **TailwindCSS** - CSS-фреймворк
- **Vanilla JavaScript** - Клиентская логика
- **Font Awesome** - Иконки

### DevOps
- **Docker** - Контейнеризация
- **PM2** - Менеджер процессов
- **Nginx** - Веб-сервер
- **Jest** - Тестирование

## 📦 Установка и запуск

### Требования
- Node.js >= 16.0.0
- PostgreSQL >= 12
- npm или yarn

### Быстрый старт

1. **Клонирование репозитория**
```bash
git clone https://github.com/KORESHon/chiwawasite.git
cd chiwawasite
```

2. **Установка зависимостей**
```bash
npm install
```

3. **Настройка окружения**
```bash
cp .env.example .env
# Отредактируйте .env файл с вашими настройками
```

4. **Создание базы данных**
```bash
npm run db:create
```

5. **Запуск в режиме разработки**
```bash
npm run dev
```

6. **Запуск в продакшене**
```bash
npm start
```

### Docker

```bash
# Сборка и запуск
npm run docker:build
npm run docker:run

# Остановка
npm run docker:stop
```

## 🔧 Конфигурация

### Переменные окружения (.env)

```env
# Сервер
PORT=3000
NODE_ENV=production

# База данных
DB_HOST=localhost
DB_PORT=5432
DB_NAME=chiwawa_db
DB_USER=your_username
DB_PASSWORD=your_password

# JWT
JWT_SECRET=your_jwt_secret
JWT_EXPIRES_IN=24h

# Email
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email
EMAIL_PASSWORD=your_app_password

# Discord (опционально)
DISCORD_WEBHOOK_URL=your_discord_webhook_url
```

## 📁 Структура проекта

```
chiwawa-server-system/
├── public/                 # Статические файлы
│   ├── index.html         # Главная страница
│   ├── login.html         # Страница входа
│   ├── register.html      # Страница регистрации
│   ├── profile.html       # Профиль пользователя
│   ├── admin.html         # Админ-панель
│   └── assets/            # Ресурсы (CSS, JS, изображения)
├── src/                   # Исходный код сервера
│   ├── server.js          # Главный файл сервера
│   ├── config/            # Конфигурация
│   ├── middleware/        # Промежуточное ПО
│   ├── models/            # Модели данных
│   ├── routes/            # Маршруты API
│   └── utils/             # Утилиты
├── database/              # База данных
│   ├── schema.sql         # Схема БД
│   └── migrations/        # Миграции
├── scripts/               # Скрипты развертывания
├── docs/                  # Документация
└── docker-compose.yml     # Docker конфигурация
```

## 🎮 API Эндпоинты

### Аутентификация
- `POST /api/auth/register` - Регистрация
- `POST /api/auth/login` - Вход
- `POST /api/auth/logout` - Выход
- `POST /api/auth/forgot-password` - Восстановление пароля

### Профиль
- `GET /api/profile` - Получить профиль
- `PUT /api/profile` - Обновить профиль
- `POST /api/profile/avatar` - Загрузить аватар

### Заявки
- `POST /api/applications` - Подать заявку
- `GET /api/applications` - Получить заявки (админ)
- `PUT /api/applications/:id` - Обновить статус заявки (админ)

### Админ
- `GET /api/admin/users` - Список пользователей
- `PUT /api/admin/users/:id` - Обновить пользователя
- `DELETE /api/admin/users/:id` - Удалить пользователя

## 🛠️ Доступные команды

```bash
# Разработка
npm run dev              # Запуск с nodemon
npm run build            # Сборка для продакшена

# Тестирование
npm test                 # Запуск тестов
npm run lint             # Линтинг кода
npm run format           # Форматирование кода

# База данных
npm run db:create        # Создание БД
npm run db:backup        # Резервное копирование

# PM2
npm run pm2:start        # Запуск с PM2
npm run pm2:stop         # Остановка PM2
npm run pm2:restart      # Перезапуск PM2
npm run pm2:logs         # Логи PM2

# Развертывание
npm run deploy:configure # Настройка развертывания
npm run deploy           # Развертывание

# Docker
npm run docker:build     # Сборка образа
npm run docker:run       # Запуск контейнера
npm run docker:stop      # Остановка контейнера
```

## 🔒 Безопасность

- Хеширование паролей с помощью bcryptjs
- JWT токены для аутентификации
- Rate limiting для предотвращения атак
- Валидация входных данных
- Защита от CSRF атак
- Secure headers с Helmet

## 🤝 Вклад в проект

1. Fork проекта
2. Создайте feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit изменения (`git commit -m 'Add some AmazingFeature'`)
4. Push в branch (`git push origin feature/AmazingFeature`)
5. Создайте Pull Request

## 📝 Лицензия

Этот проект лицензирован под MIT License - см. файл [LICENSE](LICENSE) для деталей.

## 👨‍💻 Автор

**ebluffy** - *Создатель и основной разработчик*
- Email: dima2_05@mail.ru
- GitHub: [@KORESHon](https://github.com/KORESHon)

## 🙏 Благодарности

- Minecraft сообществу за вдохновение
- Всем контрибьюторам проекта
- Игрокам сервера Chiwawa за обратную связь

## 📊 Статистика проекта

- **Версия**: 2.1.0
- **Статус**: Активная разработка
- **Последнее обновление**: Декабрь 2024

---

<div align="center">
  <p><strong>🎮 Присоединяйтесь к серверу Chiwawa уже сегодня! 🎮</strong></p>
  <p><em>Создано с ❤️ для игрового сообщества</em></p>
</div>