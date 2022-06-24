# $addTimestamp

Добавить в подвал эмбеда время вызова команды.

### Использование
 
```php
$addTimestamp[индекс;время]
```

### Опции


| Опция | Описание | Тип | Обязательно? |
|--------|-------------|------|----------|
| индекс | номер эмбеда | число | да |
| время | кастомное время | текст | нет |


## Пример:

```javascript
bot.command({
  name: 'embed-timestamp',
  code: `
  $title[1; Команда была вызвана] 
  $addTimestamp[1]
  `
});
```