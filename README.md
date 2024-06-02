## Задание 1

```javascript
function deleteAllTriggers(){
 const triggers = ScriptApp.getProjectTriggers();
 triggers.forEach(function(trigger){
   try{
     ScriptApp.deleteTrigger(trigger);
   } catch(e) {
     throw e.message;
   };
   Utilities.sleep(1000);
 });
```

Данная функция предназначена для удаления триггеров. Пошаговое выполнение:

- `function deleteAllTriggers()` - объявление функции
- `const triggers = ScriptApp.getProjectTriggers();` - получение списка всех триггеров
- `triggers.forEach(function(trigger){` - перебор всех триггеров в цикле for.

В цикле объявляется блок `try/catch` в котором производится попытка удаление триггера. В случае если при удалении
вызывается исключение, в блоке `catch` выводится сообщение об ошибке. После чего
`Utilities.sleep(1000);` приостанавливает выполнение программы.

 