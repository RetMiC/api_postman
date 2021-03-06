# Описание файла README.md


## Описание проекта
https://dummyapi.io/ представляет собой сервис для тестирования АПИ. Для выполнения запросов необходим app-id, который генерируется автоматически при регистрации на сервисе. 
В качестве тестирования были взяты следующие объекты:
### POST
____
#### GET /post (Get List)
Возвращает список публикаций отсортировнных по дате. 
- доступен query params для вывода определенной страницы.
- доступен query params для отображения числа публикаций на странице.

**Response Body**:

**List**
```javascript
{
  data: Array(Model)
  total: number(total items in DB)
  page: number(current page)
  limit: number(number of items on page)
}
```
**Data**
```javascript
{
  id: string(autogenerated)
  text: string(length: 6-50, preview only)
  image: string(url)
  likes: number(init value: 0)
  tags: array(string)
  publishDate: string(autogenerated)
  owner: object(User Preview)
}
```
____
#### POST /post/create (Create Post)
Создает новую публикацию от пользователя. Возвращает данные о публикации.

**Request Body**:



## Майнд-карта
Данная МК представляет собой набор тестов для тестирования объекта **POST**. Подробная проверка расписана для **Get List** и **Create Post**
![Alt-текст](https://i.imgur.com/k4wusSC.png "МК")

## Тест-кейсы
