# Bookmaker Ratings Widget API
## /getwidget
###### Получить массив данных для виджета.

**Метод**:
- GET

**Формат данных**:
- JSON

**Параметры**:
- bookmaker_id (required, int) - ID букмекерской конторы в БД РБ

**Возвращаемые данные**:
- bookmaker_id - ID букмекерской конторы
- name - Название букмекерской конторы
- url - URL букмекерской конторы
- feedback_url - URL формы с отзывами букмекерской конторы 
- logo - Логотип букмекерской конторы
- user_rating - Пользовательская оценка букмекерской конторы
- rb_rating - Экспертная оценка букмекерской конторы
- user_rating_count - Количество оценок пользователей

**Пример ответа**:

*JSON*:
```
{"status":"ok","data":{"bookmaker_id":309559,"name":"William Hill","url":"https:\/\/bookmaker-ratings.ru\/review\/obzor-bukmekerskoy-kontory-william-hill\/","feedback_url":"https:\/\/bookmaker-ratings.ru\/review\/obzor-bukmekerskoy-kontory-william-hill\/all-feedbacks\/?getfeedback","logo":"https:\/\/bookmaker-ratings.ru\/wp-content\/uploads\/2014\/12\/wh-logo1.png","user_rating":"3.5","rb_rating":4,"user_rating_count":318}}
```

*PHP*:
```php
array (
  'status' => 'ok',
  'data' => 
  array (
    'bookmaker_id' => 309559,
    'name' => 'William Hill',
    'url' => 'https://bookmaker-ratings.ru/review/obzor-bukmekerskoy-kontory-william-hill/',
    'feedback_url' => 'https://bookmaker-ratings.ru/review/obzor-bukmekerskoy-kontory-william-hill/all-feedbacks/?getfeedback',
    'logo' => 'https://bookmaker-ratings.ru/wp-content/uploads/2014/12/wh-logo1.png',
    'user_rating' => '3.5',
    'rb_rating' => 4,
    'user_rating_count' => 318
  ),
)
```

## /getfeedbacks
###### Получить список отзывов.

**Метод**:
- GET

**Формат данных**:
- JSON

**Параметры**:
- bookmaker_id (required, int) - ID букмекерской конторы в БД РБ
- order_by - поле сортировки отзывов (доступные значения: date, rating)
- order - порядок сортировки (ASC, DESC)

**Возвращаемые данные**:
- id - ID отзыва
- date - Дата отзыва
- author - Полное имя автора
- author_url - URL автора
- author_image_url - Аватар автора
- url - URL отзыва
- rating - Оценка
- comments - Количество комментариев к отзыву
- likes - Количество лайков
- dislikes - Количество дислайков
- text - Текст отзыва

**Пример ответа**:

*JSON*:
```
{"status":"ok","feedbacks":[{"id":1644265,"date":1532563200,"author":"\u0413\u0440\u0438\u0433\u043e\u0440\u0438\u0439 \u0413\u0440\u0438\u0448\u0438\u043d","author_url":"https:\/\/bookmaker-ratings.ru\/author\/315774\/","author_image_url":"https:\/\/pp.userapi.com\/c840230\/v840230578\/74d66\/vZmaJIwLiCQ.jpg?ava=1","url":"https:\/\/bookmaker-ratings.ru\/review\/obzor-bukmekerskoy-kontory-william-hill\/all-feedbacks\/#feedback-1644265","rating":"4.3","comments":5,"likes":1,"dislikes":0,"text":"\u041e\u0442\u043b\u0438\u0447\u043d\u0430\u044f \u043a\u043e\u043d\u0442\u043e\u0440\u0430. \u0414\u0430\u0432\u043d\u043e \u0432 \u043d\u0435\u0439 \u0441\u0442\u0430\u0432\u0438\u043b \u0438 \u0434\u043e\u043b\u0433\u043e. \u041f\u043e\u0442\u043e\u043c \u043a\u0430\u043a\u043e\u0435-\u0442\u043e \u0432\u0440\u0435\u043c\u044f \u043d\u0435 \u0441\u0442\u0430\u0432\u0438\u043b. \u0412\u043e\u0442 \u043d\u0430 \u0427\u041c-2018 \u043f\u043e\u0434\u043d\u044f\u043b \u043d\u0435\u043c\u043d\u043e\u0433\u043e \u0434\u0435\u043d\u0435\u0433. \u0417\u0430\u043f\u0440\u043e\u0441\u0438\u043b \u0432\u044b\u0432\u043e\u0434 \u0441\u0440\u0435\u0434\u0441\u0442\u0432, \u043d\u043e \u0443\u0436\u0435 \u0431\u043e\u043b\u044c\u0448\u0435 \u043d\u0435\u0434\u0435\u043b\u0438 \u043e\u043d\u0438 \u043d\u0435 \u043f\u043e\u0441\u0442\u0443\u043f\u0430\u044e\u0442 \u043d\u0430 \u0441\u0447\u0435\u0442. \u041a \u0442\u043e\u043c\u0443 \u0436\u0435, \u0447\u0435\u0440\u0435\u0437 vpn \u0431\u043e\u043b\u044c\u0448\u0435 \u043d\u0435 \u043c\u043e\u0433\u0443 \u0437\u0430\u0439\u0442\u0438 \u0442\u0443\u0434\u0430 \u0438 \u0432\u044b\u0432\u0435\u0441\u0442\u0438 \u043e\u0441\u0442\u0430\u0442\u043e\u043a. \u041f\u043e\u0434\u0441\u043a\u0430\u0436\u0438\u0442\u0435, \u043f\u043e\u0436\u0430\u043b\u0443\u0439\u0441\u0442\u0430, \u043a\u0430\u043a \u043c\u043e\u0436\u043d\u043e \u0432\u044b\u0432\u0435\u0441\u0442\u0438 \u0441\u0440\u0435\u0434\u0441\u0442\u0432\u0430? \u041c\u043e\u0436\u0435\u0442 \u0435\u0441\u0442\u044c \u0441\u0430\u0439\u0442-\u0437\u0435\u0440\u043a\u0430\u043b\u043e \u0438\u043b\u0438 \u043a\u0430\u043a\u043e\u0439-\u0442\u043e \u0434\u0440\u0443\u0433\u043e\u0439 \u0441\u043f\u043e\u0441\u043e\u0431. \u0421\u043f\u0430\u0441\u0438\u0431\u043e"}]}
```

*PHP*:

```php
array (
  'status' => 'ok',
  'feedbacks' => 
  array (
    0 => 
    array (
      'id' => 1644265,
      'date' => 1532563200,
      'author' => 'Григорий Гришин',
      'author_url' => 'https://bookmaker-ratings.ru/author/315774/',
      'author_image_url' => 'https://pp.userapi.com/c840230/v840230578/74d66/vZmaJIwLiCQ.jpg?ava=1',
      'url' => 'https://bookmaker-ratings.ru/review/obzor-bukmekerskoy-kontory-william-hill/all-feedbacks/#feedback-1644265',
      'rating' => '4.3',
      'comments' => 5,
      'likes' => 1,
      'dislikes' => 0,
      'text' => 'Отличная контора. Давно в ней ставил и долго. Потом какое-то время не ставил. Вот на ЧМ-2018 поднял немного денег. Запросил вывод средств, но уже больше недели они не поступают на счет. К тому же, через vpn больше не могу зайти туда и вывести остаток. Подскажите, пожалуйста, как можно вывести средства? Может есть сайт-зеркало или какой-то другой способ. Спасибо'
    ),
  ),
)
```

## /publishreview
###### Отправить отзыв на публикацию.

**Метод**:
- POST

**Параметры**:
- secret_key (required, string) - Уникальный ключ, дает доступ к публикации отзывов к одной (или нескольким) БК (например легальной и офшорной версии БК)
- bookmaker_id (required, int) - ID букмекерской конторы в БД РБ
- name (required, string) - Полное имя автора
- email (required, string) - Емайл автора
- rating (required, float) - Оценка
- text (required, string) - Текст отзыва

**Возвращаемые данные**:
- status - Статус отправки отзыва на публикацию (ok, error)
- error_code - Код ошибки, в случае если status не равен ok (1 - неверный ключ или ID БК не соответствует ключу, 2 - не заполнены обязательные поля, 3 - неверный формат email, 4 - ошибка сервера)

**Пример ответа**:

*JSON*:
```
{"status":"ok"}
```
