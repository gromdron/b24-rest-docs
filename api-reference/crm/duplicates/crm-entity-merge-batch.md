# Объединение дубликатов

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствуют примеры (на других языках)
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки
- не указана обязательность параметров

{% endnote %}

{% endif %}

{% note info "crm.entity.mergeBatch" %}

**Scope**: [`crm`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

```http
crm.entity.mergeBatch({params: {entityTypeId: number, entityIds: number[]}})
```
`params` - ассоциативный массив, содержащий ключи:

#|
|| **Ключ** | **Описание** ||
|| **entityTypeId**
| Идентификатор типа сущности. Может принимать значения `1` (лид), `2` (сделка), `3` (контакт) или `4` (компания) ||
|| **entityIds** 
| Массив идентификаторов элементов, которые необходимо объединить ||
|#

Метод вернет ассоциативный массив вида:

```json
{
    "STATUS": "SUCCESS",
    "ENTITY_IDS": [
        "1"
    ]
}
```

Здесь:

#|
|| **Параметр** | **Описание** ||
|| **STATUS**
| Может принимать значения:
- `SUCCESS` - объединение прошло успешно;
- `CONFLICT` - при объединении возник конфликт;
- `ERROR` - при объединении произошла ошибка. Например, если у текущего пользователя нет прав на изменение или удаление записей. ||
|| **ENTITY_IDS**
| Содержит идентификаторы элементов, которые были объединены, кроме идентификатора элемента, оставшегося после объединения. ||
|#

## Пример вызова:

```js
BX24.callMethod(
    'crm.entity.mergeBatch',
    {
        params: {
            entityTypeId: 3,
            entityIds: [1, 2, 3],
        }
    },
    (result) => {
        console.log(result);
    }
);
```

## Ручное объединение для случаев, когда возник конфликт

Для продолжения объединения вручную, в привычном пользователю интерфейсе **Битиркс24**, достаточно перенаправить его в раздел ручного объединения по соответствующей ссылке:

- Контакты: `/crm/contact/merge/?id=1,2,3`
- Компании: `/crm/company/merge/?id=1,2,3`
- Лиды: `/crm/lead/merge/?id=1,2,3`
- Сделки: `/crm/deal/merge/?id=1,2,3`

где параметр `id` содержит указанные через запятую идентификаторы объединяемых записей.





Возвращает идентификаторы лидов, контактов и компаний содержащих телефоны или email-адреса из заданного списка.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **type^*^** | Тип коммуникации:
- **EMAIL** - email-адрес;
- **PHONE** - телефон. ||
|| **values^*^** | Массив email или телефонов (до [20 значений](*ключ_значений)). Метод возвращает не более 20 дублей по сущности, причем не 20 новых, а 20 старых.

Если в сущности 20 или более дублей, результаты по остальным сущностям возвращены не будут. Например, если не указан **entity_type** и ожидаем дубли по всем трем сущностям, но у нас в лидах 20 или более дублей, сущности контакт и компания возвращены не будут. Если в сущности контакт будет 20 или более дублей, мы получим дубли по лидам и контактам, а компания будет отсутствовать в выборке. ||
|| **entity_type** | Может быть опущен, в этом случае вернутся все три типа сущности. Если параметр используется, то можно оперировать только с одним из них. Если же задать массив или несуществующий параметр, то вернутся все типы.
Типы сущности:
- **LEAD** - лид;
- **CONTACT** - контакт;
- **COMPANY** - компания. ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}

Результат возвращается в виде объекта, содержащего массивы идентификаторов лидов, контактов и компаний.

Доступ к массиву идентификаторов производится по имени типа. 

## Пример

```json
{'LEAD': [1, 2, 3], 'CONTACT': [4, 5, 6], 'COMPANY': [7, 8, 9]}
```

## Пример поиска контакта по телефону:

```js
//Поиск контакта по телефону
BX24.callMethod(
    "crm.duplicate.findbycomm",
    {
        entity_type: "CONTACT",
        type: "PHONE",
        values: [ "8976543", "11223355" ],
    },
    function(result)
    {
        if(result.error())
            console.error(result.error());
        else
            {
                console.dir(result.data());
            }
    }
);
```

{% include [Сноска о примерах](../../../_includes/examples.md) %}

[*ключ_значений]: Ограничено с целью снижения нагрузки.