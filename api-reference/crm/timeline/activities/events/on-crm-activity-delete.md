# Удаление дела

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указана обязательность параметров
- отсутствуют примеры

{% endnote %}

{% endif %}

{% note info "onCrmActivityDelete" %}

**Scope**: [`crm`](../../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Событие `onCrmActivityDelete` вызывается при удалении дела.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **FIELDS**
[`array`](../../../../data-types.md) | Массив содержит поле `ID` со значением идентификатора удалённого дела. ||
|#