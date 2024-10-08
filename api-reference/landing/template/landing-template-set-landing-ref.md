# Установка включаемых областей для страницы

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- не указана обязательность параметров
- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "landing.template.setLandingRef" %}

**Scope**: [`landing`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `landing.template.setLandingRef` устанавливает включаемые области для страницы в рамках конкретного шаблона (страница должна быть уже привязана к шаблону через поле TPL_ID). Вернет *true* в случае успеха, или ошибку.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **id**
[`unknown`](../../data-types.md) | Идентификатор страницы. ||
|| **data**
[`unknown`](../../data-types.md) | Массив данных для установки (если массив пустой или не передан, установленные области сбросятся). Ключами массива являются идентификаторы областей, а значениями идентификаторы страниц, которые необходимо установить как область. ||
|#

## Примеры

```js
BX24.callMethod(
    'landing.template.setLandingRef',
    {
        id: 557,
        data: {
            1: 614,
            2: 615,
            3: 616
        }
    },
    function(result)
    {
        if(result.error())
        {
            console.error(result.error());
        }
        else
        {
            console.info(result.data());
        }
    }
);
```

{% include [Сноска о примерах](../../../_includes/examples.md) %}