# Событие на удаление единицы измерения

> Название события: **onCrmMeasureDelete**
>
> Scope: [`crm`](../../../../scopes/permissions.md)
>
> Кто может подписаться: `любой пользователь`

Событие `onCrmMeasureDelete` вызывается после удаления единицы измерения на портале.

## Обработка ответа

HTTP-статус: **200**

Возвращает массив:

```php
array('FIELDS' => array('ID' => $id))
```

где `$id` — идентификатор удаленной единицы измерения.

## Обработка ошибок

HTTP-статус: **40x**, **50x**

В случае ошибок вызывается исключение `\Bitrix\Rest\RestException`.