# Веб-приложение блога с публикациями "Блогикум"

## Содержание
1. [Описание приложения](#описание-приложения)
2. [Установка и запуск](#установка-и-запуск)
3. [Начало работы](#начало-работы)
4. [Функционал для пользователей](#функционал-для-пользователей)
5. [Функционал для администраторов](#функционал-для-администраторов)
6. [Часто задаваемые вопросы (FAQ)](#faq)
7. [Связь с разработчиками](#связь-с-разработчиками)

---

## Описание приложения
**"Блогикум"** — это веб-приложение для ведения личных дневников и обмена контентом. Основные возможности:
- Публикация текстовых постов с медиа-вложениями (изображения, видео).
- Категоризация постов и привязка к геолокации.
- Поиск постов по категориям и географическим локациям.
- Комментирование и редактирование контента.
- Административный интерфейс для модерации и управления системой.

---

## Установка и запуск
### Требования:
- Python 3.8+.
- Браузер (Chrome, Firefox, Safari, Edge).
- Сервер Django (включён в репозиторий).

### Инструкция:
1. Клонируйте репозиторий:
  ```bash
  git clone https://github.com/BokGosha/blogicum
  ```
2. Установите зависимости:
  ```bash
  pip install -r requirements.txt
  ```
3. Запустите сервер:
  ```bash
  python manage.py runserver
  ```
4. Откройте приложение в браузере: http://localhost:8000.

---

## Начало работы
### Регистрация:
1. Перейдите на страницу регистрации: /register.
2. Вы увидите форму:
![Регистрация](https://github.com/user-attachments/assets/333629b9-0d54-4407-b19d-065847f89339)
3. Введите логин и пароль.
4. Нажмите "Зарегистрироваться".

### Авторизация:
1. Перейдите на страницу входа: /login.
2. Вы увидите форму:
![логин](https://github.com/user-attachments/assets/ce39fa92-b055-49af-b1b9-68935a8ca95a)
3. Введите логин и пароль.
4. Нажмите "Войти".

---

## Функционал для пользователей
### 1. Публикация поста  
**Шаги:**  
- Перейдите на страницу создания поста: `/create-post`.
- Вы увидете форму:
![создание поста](https://github.com/user-attachments/assets/80f97ab4-bc6d-462e-a1d7-34c95f83e94c)
- Заполните поля:  
  - **Заголовок:** краткое описание поста (например, *"Моё путешествие в Париж"*).  
  - **Текст:** основной контент (до 5000 символов).
  - **Дата и время:** время когда выкладываете пост.
  - **Местоположение:**  
    - Введите название места (например, *"Елисейские поля"*).  
  - Нажмите **"Опубликовать"**. Пост появится в ленте.  

### 2. Поиск постов  
**По категориям:**  
- Перейдите в меню **"Категории"**.  
- Выберите категорию (например, *"Еда"*).  
- Результаты отобразятся в хронологическом порядке.  

**По геолокации:**  
- На главной странице выберите **"Фильтр по местоположению"**.  
- Введите название города или координаты.  
- Посты, связанные с выбранной локацией, отобразятся в списке.  

### 3. Редактирование и удаление постов  
**Редактирование:**  
- Перейдите на страницу поста.  
- Нажмите **"Изменить"** (иконка ручки в углу).  
- Отредактируйте текст, медиа или метаданные.  
- Нажмите **"Сохранить изменения"**.  

**Удаление:**  
- Перейдите на страницу поста.  
- Нажмите **"Удалить"** (иконка корзины).  
- Подтвердите действие в диалоговом окне.  

### 4. Комментарии  
**Добавление комментария:**  
- Откройте пост.  
- Введите текст в поле **"Добавить комментарий"**.  
- Нажмите **"Отправить"**.  

**Редактирование/удаление комментария:**  
- Наведите курсор на свой комментарий.  
- Нажмите **"Изменить"** или **"Удалить"**.  
- Для удаления подтвердите действие.  

---

## Функционал для администраторов
### 1. Модерация контента
- **Утверждение/удаление постов**:
  1. В админ-панели выберите пост.
  2. Нажмите **"Одобрить"** (для публикации) или **"Удалить"**.
  3. Для удаления укажите причину (например, "Нарушение правил") в поле **"Комментарий"**.
  4. Подтвердите действие в диалоговом окне: **"Да, удалить"**.

- **Массовая модерация**:
  1. Выделите несколько постов, используя чекбоксы.
  2. Выберите действие: **"Одобрить все"** или **"Удалить все"**.
  3. Подтвердите выбор в окне подтверждения.

### 2. Управление пользователями
- **Просмотр профилей**:
  1. Перейдите в раздел **"Пользователи"**.
  2. Нажмите на логин пользователя для детального просмотра:
     - История постов.
     - Активность (последний вход, количество комментариев).
     - Роль (пользователь/админ).
- **Блокировка/разблокировка**:
  1. В списке пользователей найдите нужного.
  2. Нажмите **"Блокировать"** (для временной блокировки) или **"Разблокировать"**.
  3. Укажите срок блокировки (например, "24 часа") и причину.
- **Изменение ролей**:
  1. Выберите пользователя.
  2. В поле **"Роль"** выберите новое значение (например, "Администратор").
  3. Сохраните изменения.

### 3. Управление категориями
- **Создание категории**:
  1. Перейдите в раздел **"Категории"**.
  2. Нажмите **"Добавить категорию"**.
  3. Введите название и описание (например, "Наука" — "Статьи о технологиях").
  4. Нажмите **"Сохранить"**.
- **Редактирование категории**:
  1. Выберите категорию в списке.
  2. Измените название/описание.
  3. Нажмите **"Обновить"**.
- **Удаление категории**:
  1. Выберите категорию.
  2. Нажмите **"Удалить"**.
  3. Подтвердите действие. Все посты в этой категории останутся, но категория будет удалена.

---

## FAQ
**Вопрос:** Как восстановить удаленный пост?  
**Ответ:**  
1. Перейдите в админ-панель → **"Удаленные посты"**.  
2. Найдите пост в списке.  
3. Нажмите **"Восстановить"** и укажите причину.

**Вопрос:** Как изменить порядок отображения постов в ленте?  
**Ответ:**  
Администратор может:
1. В настройках системы выбрать сортировку:  
   - По дате (по умолчанию).  
   - По количеству лайков.  
   - По алфавиту.

**Вопрос:** Как добавить новую роль пользователя?  
**Ответ:**  
1. В админ-панели → **"Роли"**.  
2. Нажмите **"Создать роль"**.  
3. Укажите права (например, "Модератор комментариев").  
4. Присвойте роль пользователю через его профиль.

**Вопрос:** Как ограничить доступ к определенной категории?  
**Ответ:** 
1. Перейдите в **"Категории"**.  
2. Выберите категорию → включите **"Ограниченный доступ"**.  
3. Укажите роли, которым разрешен доступ (например, "Администраторы").

---

## Связь с разработчиками
- **Email**: support@belkovye-bomby.ru
- **GitHub**: [репозиторий](https://github.com/BokGosha/blogicum)  
- **Телеграм**: @belkovye_bomby_support
