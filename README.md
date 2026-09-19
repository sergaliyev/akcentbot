# WhatsApp Bot (Node.js + TypeScript)

Бот для WhatsApp на базе библиотеки `@whiskeysockets/baileys`.

## Структура проекта

```text
├── src/
│   ├── index.ts              # Точка входа
│   ├── config/               # Конфигурация, меню, тексты ответов
│   ├── core/                 # Подключение к WhatsApp (Baileys), управление сессией
│   ├── handlers/             # Обработчики входящих сообщений и FSM
│   └── services/             # Отправка заявок (Telegram, CRM, Sheets)
├── auth_info_baileys/        # Данные сессии WhatsApp (в .gitignore, не публиковать!)
├── .env.example              # Пример переменных окружения
├── package.json              # Зависимости
└── tsconfig.json             # Настройки TypeScript
```

## Установка и запуск

1. Установка зависимостей:
   ```bash
   npm install
   ```

2. Запуск в режиме разработки:
   ```bash
   npm run dev
   ```

3. Сборка и запуск продакшн:
   ```bash
   npm run build
   npm start
   ```

## Подключение номера WhatsApp
При первом запуске в терминале отобразится QR-код:
1. Откройте WhatsApp на телефоне.
2. Перейдите в **Связанные устройства** (`Linked devices`).
3. Нажмите **Привязать устройство** (`Link a device`) и отсканируйте QR-код из терминала.
4. Сессия сохранится локально в папке `auth_info_baileys/`, повторное сканирование при перезапуске не потребуется.
