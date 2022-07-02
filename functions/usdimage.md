# $image

Добавляет ссылку к эмбед сообщению

### Использование
 
```php
$image[индекс;ссылка]
```

### Опции


| Опция | Описание | Тип | Обязательно? |
|--------|-------------|------|----------|
| индекс | номер эмбеда | число | да |
| ссылка | ссылка на изображение | ссылка | да |


## Пример:

```javascript
bot.command({
  name: 'embed-image',
  code: `
  $image[1;$useravatar]
  `
});
```