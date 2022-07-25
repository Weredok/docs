# $apiMessage
Отправляет сообщение при помощи возможностей Дискорд АПИ
### Использование
```php
$apiMessage[канал;контент;эмбеды?;компоненты?;файлы?;стикеры?;упоминания?;ответ?;вернутьАйди?]
```

### Опции

| Опция | Описание | Тип | Обязательно |
|--------|-------------|------|----------|
| канал | айди канала, в который нужно отправить сообщение | айди | Да | 
| контент | контент сообщения | текст | Да | 
| эмбеды | встроенные сообщения | текст | Нет |
| компоненты | компоненты сообщения | текст | Нет |
| файлы | файлы сообщения | текст | Нет |
| стикеры | стикеры сообщения | айди | Нет |
| упоминания | разрешить ли упоминания в сообщении | логическое выражение | Нет |
| ответ | ответить ли на сообщение, которое вызвало эту функцию | логическое выражение | Нет |
| вернутьАйди | вернуть ли айди сообщения | логическое выражение | Нет |
## Пример(ы)

```javascript
bot.command({
  name: '$apiMessage',
  code: `
$apiMessage[$channelID;Hello, World!;{newEmbed:{title: l }};{actionRow:{button:Hi:1:hi}{button:Bye:2:bye}};{attachment:$authorAvatar:avatar.png};9855473711203379;yes;yes;yes]`
// Возвращает: 984566341245090017
})
```