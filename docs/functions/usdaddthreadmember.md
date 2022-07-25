# $addThreadMember
Добавляет участника сервера к ветке
### Использование
```php
$addThreadMember[канал;ветка;пользователь;причина]
```

### Опции

| Опция | Описание | Тип | Обязательно |
|--------|-------------|------|----------|
| канал | канал, к которому привязана ветка | айди | Да | 
| ветка | ветка, в которую нужно добавить участника | айди | Да | 
| пользователь | пользователь, которого нужно добавить в ветку | айди | Да |
| причина | причина добавления, которая отобразится в журнале аудита | текст | Да |