# Изменение состояния интерфейса карточки звонка со стороны приложения

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "CallCardSetUiState" %}

{% include notitle [Скоуп telephony all](../../../telephony/_includes/scope-telephony-all.md) %}

{% endnote %}

Метод `CallCardSetUiState` позволяет со стороны приложения изменить состояние интерфейса карточки звонка.

Приложение должно передавать в метод объект со свойством uiState, значение которого должно одним из получаемых из метода getListUiStates. В функцию обратного вызова не передаются какие-либо данные.

## Пример

```js
BX24.placement.bindEvent('BackgroundCallCard::initialized', event => {
    BX24.placement.call(CallCardSetUiState', {uiState: 'connected'}, () => {
        // some code 
    })
});
```

{% include [Сноска о примерах](../../../../_includes/examples.md) %}