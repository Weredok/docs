
# $description

Добавить описание для указанного эмбеда

### Использование
 
```php
$description[индекс;текст]
```

### Опции


| Опция | Описание | Тип | Обязательно? |
|--------|-------------|------|----------|
| индекс | номер эмбеда | число | да |
| текст | описание эмбеда | текст | да |


## Пример:

```javascript
bot.command({
  name: 'embed-description',
  code: `
  $description[1;А что тут писать?]
  `
});
```