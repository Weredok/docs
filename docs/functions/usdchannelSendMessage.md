# $channelSendMessage

Отправить сообщение от имени бота в указанный канал.

### Использование
 
```php
$channelSendMessage[канал;сообщение;вернуть айди]
```

### Опции


| Опция | Описание | Тип | Обязательно? |
|--------|-------------|------|----------|
| канал | индетификатор текстового канала | канал | да |
| сообщение | контент сообщения | текст | да |
| вернуть айди | бот отправит айди сообщения которое он написал | число | нет | 


## Пример:

```javascript
bot.command({
  name: 'channel-send-message',
  code: `
  $channelSendMessage[$channelid;$message]
  `
});
```
