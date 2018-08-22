# Bookmaker Ratings Widget API
## /getwidget
###### Получить массив данных для виджета.

Метод:
- GET

Формат данных:
- JSON

Параметры:
- bookmaker_id (required, int) - ID букмекерской конторы в БД РБ

Возвращаемые данные:
- bookmaker_id - ID букмекерской конторы
- name - Название букмекерской конторы
- url - URL букмекерской конторы
- feedback_url - URL формы с отзывами букмекерской конторы 
- logo - Логотип букмекерской конторы
- user_rating - Пользовательская оценка букмекерской конторы
- rb_rating - Экспертная оценка букмекерской конторы
- user_rating_count - Количество оценок пользователей

Пример ответа:
```
{"status":"ok","data":{"bookmaker_id":309559,"name":"William Hill","url":"https:\/\/bookmaker-ratings.ru\/review\/obzor-bukmekerskoy-kontory-william-hill\/","feedback_url":"https:\/\/bookmaker-ratings.ru\/review\/obzor-bukmekerskoy-kontory-william-hill\/all-feedbacks\/?getfeedback","logo":"https:\/\/bookmaker-ratings.ru\/wp-content\/uploads\/2014\/12\/wh-logo1.png","user_rating":"3.5","rb_rating":4,"user_rating_count":318}}
```

