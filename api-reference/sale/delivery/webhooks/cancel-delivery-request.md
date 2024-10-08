# Отменить заказ на доставку

Запрос отправляется на адрес указанный в `CANCEL_DELIVERY_REQUEST_URL` при создании обработчика доставки в методе [sale.delivery.handler.add](../handler/sale-delivery-handler-add.md).

## Параметры запроса

#|
|| **Название**
`тип` | **Описание** ||
|| **DELIVERY_ID**
[`sale_delivery_service.ID`](../../data-types.md#sale_delivery_service) | Идентификатор службы доставки.

Получить идентификаторы служб доставки можно с помощью метода [sale.delivery.getlist](../delivery/sale-delivery-get-list.md)
 ||
|| **REQUEST_ID**
[`string`](../../../data-types.md) | Идентификатор транспортной заявки.

Идентификатор назначается внешней системой в ответе вебхука на создание заказа на доставку (детальнее смотрите в описании вебхука [{#T}](./create-delivery-request.md))
 ||
|#

## Пример запроса

```json
{
    "DELIVERY_ID": 694,
    "REQUEST_ID": "4757aca4931a4f029f49c0db4374d13d",
}
```

## Параметры ответа

{% include [Сноска об обязательных параметрах](../../../../_includes/required.md) %}

#|
|| **Название**
`тип` | **Описание** ||
|| **SUCCESS***
[`string`](../../../data-types.md) | Индикатор успеха отмены заказа на доставку. Возможные значения:

- `Y` — заказ успешно отменен
- `N` — произошла ошибка при попытке отмены заказа
 ||
|| **REASON**
[`object`](../../../data-types.md) | Причина ошибки. Передается в случае неудачной попытки отмены заказа на доставку (подробное описание приведено [ниже](#reason)) ||
|#

### REASON

#|
|| **Название**
`тип` | **Описание** ||
|| **TEXT***
[`string`](../../../data-types.md) | Описание ошибки ||
|#

## Пример ответа с успешным созданием заказа на доставку

```json
{
    "SUCCESS": "Y"
}
```

## Пример ответа с ошибкой при расчете стоимости

```json
{
    "SUCCESS": "N",
    "REASON": {
        "TEXT": "The order has been already delivered"
    }
}
```

## Продолжите изучение 

- [{#T}](./index.md)
- [{#T}](./calculate.md)
- [{#T}](./create-delivery-request.md)