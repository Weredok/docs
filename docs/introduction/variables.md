# Переменные
В этой статье будет рассказано о работе переменных в библиотеке.

Создавать переменные можно при помощи функции в главном файле:
```javascript
bot.variables({
  название: "значение",
  название2: "значение2"
})
```
Переменные хранятся в базе данных по данным, которые устанавливаются функциями, например:
```javascript
$setUserVar[abc;dfg]
```
Переменная abc теперь имеет значение dfg для пользователя, который вызвал функцию. Если мы запросим получение - мы получим то же значение, что и устанавливалось. Если же значения нету - мы получим станлартное значение, которое указывается при создании переменных. Если вы хотите сделать проверку на стандартное значение, то можно сделать так:
```javascript
$if[$getUserVar[abc]!=$getVar[abc];Переменная не равна стандартному значению;Переменная равна стандартному значению]
```
```javascript
$getUserVar[abc] //Вернёт dfg
```
Вы можете привязывать значения к любому айди, или слову, но рекомендуется использовать функции по их назначению.

## Переменные для сообщений
Вы можете использовать переменные, привязывая их к айди сообщения. Вот обычные примеры работы для сообщений:
```javascript
$setMessageVar[abc;456] //Привязывает значение переменной abc для сообщения, которое вызвало функцию
```
```javascript
$getMessageVar[abc] //Вернёт значение переменной для сообщения, которое вызвало функцию
```
  Точно так-же работают и переменные для каналов и серверов

## Пользовательские переменные

По-умолчанию обычные пользовательские переменные привязываются к серверам. Тоесть, если у пользователя на одном сервере переменная будет значению dfg, это не значит что на другом сервере у него будет такое же значение. Для этого нужно использовать глобальные пользовательские переменные, о них написано ниже

## Глобальные пользовательские переменные
У этого типа перменных есть две важные способности:
* Установка значения для всех пользователей, если не указывать айди участника
* Установка значения только для одного пользователя для всех серверов

Установка значения для всех пользователей, произойдёт если мы не укажем пользователя в функции:
```javascript
$setGlobalUserVar[abc;hjk]
```
У всех пользователей теперь будет установлено узначение hjk

Поэтому, если вы хотите указать значение только для автора - указывайте его айди в функции:
```javascript
$setGlobalUserVar[abc;hjk;$authorID]
```