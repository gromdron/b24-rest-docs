# Отменить регистрацию коннектора

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны тип и обязательность параметров
- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки
  
{% endnote %}

{% endif %}

{% note info "imconnector.unregister" %}

**Scope**: [`imopenlines`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод удаления коннектора.

#|
|| **Параметр** | **Описание** | **С версии** ||
|| **ID**
[`unknown`](../../data-types.md) | Уникальный идентификатор коннектора. | ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}