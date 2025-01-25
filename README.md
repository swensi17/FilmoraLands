# 🎬 FilmoraLands — Кинотека нового поколения

[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-%233776AB?logo=python)](https://www.python.org/)
[![Flask 2.0.1](https://img.shields.io/badge/Flask-2.0.1-%23000?logo=flask)](https://flask.palletsprojects.com/)
[![License MIT](https://img.shields.io/badge/License-MIT-%23brightgreen)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/swensi17/FilmoraLands?style=social)](https://github.com/swensi17/FilmoraLands/stargazers)

**Ваш персональный гид в мире кино!**  
Поиск фильмов, трейлеры в HD, актерские составы и умные рекомендации — всё в одном месте.

---

## 🌟 Ключевые возможности

### 🎥 Основные функции
- **Умный поиск** с автодополнением и фильтрацией
- **Детализация фильмов**: 
  - Рейтинг TMDB с анимацией
  - Полные метаданные (год, жанры, описание)
  - Актерский состав с фото
- **Трейлеры 4K** с приоритетом русской озвучки
- **Персонализированные рекомендации** на основе AI

### 🎨 Уникальные фишки
```css
/* Интерактивные элементы */
.movie-card {
  transform: scale(1);
  transition: all 0.3s ease;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.movie-card:hover {
  transform: scale(1.05);
  box-shadow: 0 12px 40px rgba(33, 208, 122, 0.2);
}
```
- Анимированные hover-эффекты
- Адаптивная сетка постеров
- Кастомные модальные окна с параллаксом
- Ночной режим (в разработке 🔧)

---

## 🛠 Технологический стек

### Backend
| Технология       | Назначение                     |
|------------------|--------------------------------|
| Python 3.10      | Ядро приложения               |
| Flask 2.0        | Веб-фреймворк                |
| Requests         | Работа с TMDB API            |
| python-dotenv     | Управление переменными среды |

### Frontend
```html
<!-- Пример компонента -->
<div class="movie-card" data-rating="8.5">
  <div class="rating-badge">
    <i class="fas fa-star"></i>
    <span>8.5</span>
  </div>
</div>
```
- Bootstrap 5 + кастомные стили
- Font Awesome 6 иконки
- YouTube Player API
- Адаптивная верстка

---

## 🚀 Быстрый старт

### Требования
- Python 3.8+
- API ключ TMDB ([получить](https://www.themoviedb.org/documentation/api))

### Установка за 5 минут
1. Клонируйте репозиторий:
```bash
git clone https://github.com/swensi17/FilmoraLands.git && cd FilmoraLands
```

2. Настройте окружение:
```bash
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
```

3. Создайте `.env` файл:
```ini
FLASK_APP=main.py
FLASK_ENV=development
TMDB_API_KEY=ваш_ключ
```

4. Запустите сервер:
```bash
flask run --host=0.0.0.0 --port=5000
```

---

## 🎮 Как пользоваться

### Основные сценарии
1. **Поиск фильмов**  
   Введите название в поисковую строку → получите grid-галерею

2. **Просмотр деталей**  
   Клик на постер →  
   ✔️ Трейлер в HD  
   ✔️ Актерский состав с биографиями  
   ✔️ Полная информация о франшизе

3. **Работа с API**  
Пример запроса к TMDB API:
```python
@app.route('/movie/<int:movie_id>')
def get_movie(movie_id):
    response = requests.get(
        f"{BASE_URL}/movie/{movie_id}",
        params={"api_key": API_KEY, "language": "ru-RU"}
    )
    return render_template('movie.html', movie=response.json())
```

---

## 🛠 Архитектура проекта

```
FilmoraLands/
├── static/
│   ├── css/
│   │   └── style.css       # Кастомные стили
│   └── js/
│       └── script.js       # Интерактивные элементы
├── templates/
│   ├── movie.html          # Детали фильма
│   └── search.html         # Страница поиска
├── main.py                 # Ядро приложения
└── requirements.txt        # Зависимости
```

---
## Использование

- **Поиск фильмов:** Введите название фильма в поисковую строку и нажмите "Поиск".
- **Просмотр деталей:** Нажмите на постер фильма, чтобы открыть детальную страницу с информацией и трейлером.
- **Жанры:** Перейдите в раздел "Жанры" для фильтрации фильмов по категориям.
- **Аниме:** Специальный раздел для поиска и просмотра аниме.

## Вклад

Мы приветствуем ваши предложения и вклады! Пожалуйста, следуйте этим шагам для внесения изменений:

1. **Создайте форк репозитория.**
2. **Создайте новую ветку для вашей функциональности:**

    ```bash
    git checkout -b feature/YourFeatureName
    ```

3. **Внесите изменения и зафиксируйте их:**

    ```bash
    git commit -m "Добавлена новая функция"
    ```

4. **Отправьте изменения в свой форк:**

    ```bash
    git push origin feature/YourFeatureName
    ```

5. **Создайте Pull Request на GitHub.**

## Контакты

Если у вас есть вопросы или предложения, вы можете связаться со мной по следующим каналам:

- **Email:** [tutatutaev9@gmail.com](mailto:your_email@example.com)
- **GitHub:** [swensi17](https://github.com/swensi17)
- **Telegram:** [swensi17](https://t.me/swensi17)

---

