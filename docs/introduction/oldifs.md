 # $if: "v4"
 Включает старое использование функции $if и её подобных. 

{ % hint style='warning' % } В этих функциях не работает следующий ряд функций: $let и $get, все функции которые зависят от обратных вызовов (такие как $newRole, $newGuild и подобные), функции которые выдают инфоомацию о интерактиве (такие как $interactionData, $slashOption, $getApplicationCommandID и подобные) { % endhint % }

 ## Дополнительные функции
* `$endif` - закрывает код, который выполнится в условии

* `$elseif[условие]` - открывает блок кода, который выполнится если условие в $if неправильное

* `$endelseif` - закрывает блок кода условия, которое выполняется если условие в $if неправильное

* `$else` - создает блок кода, который выполнится если условие в $id неправильное, при любом значении]

## Примеры использований
1. Проверяет, является ли сообщение числом
```javascript
module.exports = {
name: "if",
$if: "v4",
code: `$if[$isNumber[$message]==true;]
Это число!
$else
Это не число!
$endif`
}
```
2. Проверяет какое число указал пользователь
```javascript
module.exports = {
name: "if2",
$if: "v4",
code: `$if[$message[1]==1;]
Число, которое Вы указали равно 1
$elseif[$message[1]==2]
Число, которое Вы указали равно 2
$endelseif
$else
Число которое Вы указали не равно ни 1 ни 2
$endif`
}
```
3. Отвечает на слово "привет"
```javascript
module.exports = {
name: "if3",
$if: "v4",
code: `$if[$message==привет;]
Привет!
$endif`
}
```
