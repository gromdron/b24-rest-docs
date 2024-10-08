# Удаление зарегистрированного обработчика места встраивания

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- нужны правки под стандарт написания
- не указаны типы параметров
- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "placement.unbind" %}

**Scope**: [`в зависимости от места встройки`](../scopes/permissions.md) | **Кто может выполнять метод**: `администратор`

{% endnote %}

Метод удаляет зарегистрированный обработчик места встраивания и возвращает количество удаленных обработчиков.

## Параметры

#|
|| **Параметр** | **Описание** | **С версии** ||
|| **PLACEMENT**^*^ | Идентификатор места встраивания.  | ||
|| **HANDLER** | URL обработчика места встраивания. Если не указывать URL обработчика, будут удалены все обработчики указанного места встраивания, зарегистрированные приложением. | ||
|#

\* - Обязательный параметр.


## Пример

```http
GET https://sometestportal.bitrix24.com/rest/placement.unbind?auth=7e623a5a0000cd710000cd5b00000001000000a8b1dbe022e2de93198634e9526b00f7&placement=CRM_LEAD_DETAIL_TAB&handler=https%3A%2F%2Fwww.myapplicationhost.com%2Fplacement%2F HTTP/1.1
HTTP/1.1 200 OK
{
    "result": {
        "count": 1
    }
}
```

{% include [Сноска о примерах](../../_includes/examples.md) %}