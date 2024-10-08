# Блок со ссылками

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- нужны правки под стандарт написания

{% endnote %}

{% endif %}

![Блок со ссылками](./_images/link.png)

`LINK` - вывод блока с ссылкой на ресурс, описанием и картинкой-пояснением. Этот блок используется при автоматическом создании «богатых ссылок».

Поля **DESC** (описание) и **PREVIEW** (картинка) не являются обязательными полями.

Поля **WIDTH** (ширина) и **HEIGHT** (высота) не являются обязательными, но рекомендуется их указывать уже сейчас, чтобы правильно отобразить изображение.

## Пример

{% list tabs %}

- JS

    ```js
    {
        LINK: {
            PREVIEW: "https://dev.1c-bitrix.ru/bitrix/templates/1c-bitrix-new/images/logo.png",
            WIDTH: 1000,
            HEIGHT: 638,
            NAME: "Тикет #12345: новое API для модуля \"Веб-мессенджер\"",
            DESC: "Необходимо реализовать к релизу!",
            LINK: "https://api.bitrix24.com/",
        }
    },
    ```

- PHP

    ```php
    Array(
        "LINK" => Array(
            "PREVIEW" => "https://dev.1c-bitrix.ru/bitrix/templates/1c-bitrix-new/images/logo.png",
            "WIDTH" => "1000",
            "HEIGHT" => "638",
            "NAME" => "Тикет #12345: новое API для модуля \"Веб-мессенджер\"",
            "DESC" => "Необходимо реализовать к релизу!",
            "LINK" => "https://api.bitrix24.com/"
        )
    ),
    ```

{% endlist %}

{% include [Сноска о примерах](../../../../../_includes/examples.md) %}

Вместо ключа **LINK** можно использовать и ссылки на сущности:
- `CHAT_ID => 1` - для указания ссылки на чат;
- `USER_ID => 1` - для указания ссылки на пользователя.