# $attachment
Отправляет сообщение с вложенным файлом. Это может быть как текстовый файл, так и картинка.
### Использование
```php
$attachment[вложение;название;тип?]
```

### Опции

| Опция | Описание | Тип | Обязательно |
|--------|-------------|------|----------|
| вложение | ссылка или путь файла, который нужно вложить | ссылка | Да | 
| название | название файла, которое отобразится при отправке | текст | Да | 
| тип | тип вложения | текст | Нет |
## Пример(ы)

```javascript
bot.command({
  name: '$attachment',
  code: `
$attachment[$authorAvatar;avatar.png;image]`
})
```