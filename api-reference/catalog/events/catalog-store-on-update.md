# При изменении склада

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы полей
- не указана обязательность полей
- отсутствуют примеры

{% endnote %}

{% endif %}

{% note info "CATALOG.STORE.ON.UPDATE" %}

**Scope**: [`catalog`](../../scopes/permissions.md) | **Кто может подписаться**: `любой пользователь`

{% endnote %}

Событие `CATALOG.STORE.ON.UPDATE` срабатывает при изменении склада. В обработчик передаются следующие данные:

#|
|| **Поле** | **Описание** ||
|| **ID** | Идентификатор сущности, по которой сработало событие. ||
|#