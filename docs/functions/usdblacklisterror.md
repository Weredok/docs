# $blacklistError
Отправляет сообщение о том что пользователь находится в чёрном списке. Чтобы установить чёрный список, используйте функцию [$blacklist](functions/usdblacklist.md).
### Использование
```php
$blacklistError[тип;сообщение?]
```

### Опции

| Опция | Описание | Тип | Обязательно |
|--------|-------------|------|----------|
| тип | тип чёрного списка | текст | Да | 
| сообщение | сообщение о том что пользователь в чёрном списке | сообщение | Нет | 
## Пример(ы)

```javascript
bot.command({
  name: '$blacklist',
  code: `$blacklistError[Отказано в доступе]
$blacklist[user;$userID[someone]]`
// Возвращает: Отказано в доступе
})
```