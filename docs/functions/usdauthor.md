# $author
Создаёт поле автора в встроенном сообщении
### Использование
```php
$author[индекс?;текст;изображение?;ссылка?]
```

### Опции

| Опция | Описание | Тип | Обязательно |
|--------|-------------|------|----------|
| индекс | индекс встроенного сообщения | число | Да |  
| текст | отображаемый текст на поле | текст | Да |  
| изображение | отображаемое изображение сбоку от текста | ссылка | Да |  
| ссылка | ссылка, по которой перейдёт пользователь при нажатии на текст | ссылка | Да |  
## Пример(ы)

```javascript
bot.command({
  name: '$author',
  code: `
$author[1;$userTag;$authorAvatar]`
})
```