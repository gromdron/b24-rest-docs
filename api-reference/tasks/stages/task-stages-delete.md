# Удаление стадии Канбана / Моего плана

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- не указана обязательность параметров
- отсутствуют примеры (должно быть три примера - curl, js, php)
- отсутствует ответ в случае ошибки
- отсутствует ответ в случае успеха
 
{% endnote %}

{% endif %}

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% note info "task.stages.delete" %}

**Scope**: [`task`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `task.stages.delete` удаляет стадию Канбана / Моего плана.  Принимает на вход `id` стадии.

Стадия проверяется на достаточный уровень прав, а также на то, что в ней нет задач

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **id**
[`unknown`](../../data-types.md) | Идентификатор стадии, которую необходимо удалить. ||
|| **isAdmin**
[`unknown`](../../data-types.md) | Если установлено `true`, то проверки прав происходить не будет, при условии, что запрашивающий является администратором портала. ||
|#

Возвращает `true` в случае успешного удаления стадии.