# Групповой импорт записей

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указана обязательность параметров
- отсутствуют примеры на др. языках
- отсутствует ответ в случае ошибки
- спросить у разработчика (Зылёв) про синтаксис

{% endnote %}

{% endif %}

{% note info "crm.item.batchImport" %}

**Scope**: [`crm`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

```http
crm.item.batchImport({entityTypeId: number, $data: ?{})
```

Групповой импорт записей.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **entityTypeId** | Идентификатор типа элемента ([Какие сущности поддерживаются?](index.md)) ||
|| **data** | Массив значений полей элементов. Можно рассматривать его как массив, каждый элемент которого содержит набор полей `fields`, описанный в методе [crm.item.import](crm-item-import.md). ||
|#

{% include [Сноска о параметрах](../../../../_includes/required.md) %}

Метод вернет массив `data`, содержащий те же ключи, которые были в массиве `data` запроса. Каждый элемент этого массива будет содержать результат импорта конкретного элемента: массив `item` с идентификатором созданного элемента в случае успеха, либо сообщение об ошибке.

Логика добавления элементов работает по аналогии с методом [crm.item.import](crm-item-import.md).

{% note warning "Внимание!" %}

В одном запросе допустимо импортировать максимум 20 элементов.

{% endnote %}

## Пример

Импорт сделки:

```json
{
    "entityTypeId": 2,
    "data": [
        {
            "title": "Моя сделка",
            "categoryId": 0
        },
        {
            "title": ""
        }
    ]
}
```

**Пример результата:**

```json
{
    "result": {
        "items": [
            {
                "item": {
                    "id": 15
                }
            },
            {
                "error": "CRM_FIELD_ERROR_REQUIRED",
                "error_description": "Поле \"Название\" обязательно для заполнения"
            }
        ]
    }
}
```

{% include [Сноска о примерах](../../../../_includes/examples.md) %}