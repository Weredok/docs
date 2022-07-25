# $awaitComponents
Начинает ожидание взаимодействия пользователя с компонентами. Если нужно отслеживать действия от всех пользователей - укажите в опции фильтра everyone.
### Использование
```php
$awaitComponents[сообщение;фильтр;названия;команды;ошибка;использования;данные]
```

### Опции

| Опция | Описание | Тип | Обязательно |
|--------|-------------|------|----------|
| сообщение | отслеживаемое сообщение | айди | Да | 
| фильтр | фильтр пользователей, которых нужно отслеживать | айди | Да | 
| названия | названия компонентов | перечисление | Да |
| команды | названия ожидаемых команд | перечисление | Да |
| ошибка | ошибка, если нету таких названий компонентов или команд | текст | Нет |
| использований | количество отслеживаемых использований | число | Нет |
| данные | данные для ожидаемых команд | объект | Нет |
## Пример(ы)

```javascript
bot.command({
  name: '$awaitComponents',
  code: `
$awaitComponents[$messageID;everyone;hi;bye;gn; l ;1;{}]
Hi 
$addButton[1;Hi;2;hi]
$addButton[1;Bye;2;bye]`
})
```