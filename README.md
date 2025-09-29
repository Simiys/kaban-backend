# Kaban X – Backend

## 📖 Описание проекта
Kaban X – это система управления проектами в формате канбан-доски. Пользователь может создать проект (с автоматической доской), пригласить участников и назначать им задания.

## 🛠️ Стек технологий
- Python
- FastAPI
- MySQL
- SQLAlchemy
- Docker

## 👥 Роли пользователей и сценарии
- **Владелец проекта** – создаёт проект, управляет доской, приглашает пользователей, назначает задания.
- **Приглашённый пользователь** – принимает приглашения, работает с заданиями в рамках проекта.

## 🗄️ Схема БД
![ER-диаграмма](https://drawsql.app/teams/soundcloud-fm/diagrams/kaban)

## 🔗 API
| Метод | URL | Описание |
|-------|-----|----------|
| POST | /auth/register | Регистрация |
| POST | /auth/login | Вход |
| POST | /auth/refresh | Обновление токена |
| GET | /user/me | Получить свои данные |
| POST | /projects | Создать проект |
| GET | /projects | Список проектов |
| GET | /projects/{id} | Получить проект |
| POST | /projects/{id}/invite | Пригласить пользователя |
| GET | /projects/{id}/board | Получить доску проекта |
| POST | /projects/{id}/sections | Добавить колонку |
| PATCH | /projects/{id}/sections/{section_id} | Обновить колонку |
| POST | /projects/{id}/tasks | Создать задачу |
| PATCH | /projects/{id}/tasks/{task_id} | Обновить задачу |
