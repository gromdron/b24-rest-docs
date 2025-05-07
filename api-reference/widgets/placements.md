# Места для встройки виджетов

Практически в каждом инструменте Битрикс24 существуют места для встройки виджетов. 

Каждое приложение может зарегистрировать неограниченное количество виджетов, причём даже одного типа, если место для встройки в принципе это позволяет. Например, одно приложение может добавить несколько закладок в карточку сделки. Или несколько пунктов выпадающего контекстного меню в списке задач и т.д.

{% note info "mobile" %}

Некоторые места встроек еще не выпущены или имеют особенный механизм работы, поэтому на данной странице они не отображены:
- [Пользовательские типы полей в CRM](./user-field/index.md)
- [Мессенджер](./im/index.md)
- [Универсальные виджеты](./universal/app-url.md)

{% endnote %}


#|
|| *[CRM](./crm/index.md)*  | >            ||
|| Код {.cell-align-center} | Примечание {.cell-align-center} ||
|| `CRM_XXX_LIST_MENU`  | Пункт [контекстного меню](*CRM_XXX_LIST_MENU) в списке элементов ||
|| `CRM_XXX_LIST_TOOLBAR`  | Пункт [выпадающего меню](*CRM_XXX_LIST_TOOLBAR) над списком элементов ||
|| `CRM_XXX_DETAIL_TAB`  | [Вкладка](*CRM_XXX_DETAIL_TAB) в детальной карточке элемента CRM ||
|| `CRM_XXX_DETAIL_ACTIVITY` | [Кнопка](*CRM_XXX_DETAIL_ACTIVITY) над таймлайном карточки элемента ||
|| `CRM_XXX_DETAIL_TOOLBAR` | [Пункт выпадающего меню](*CRM_XXX_DETAIL_TOOLBAR) верхней кнопки карточки элемента ||
|| `CRM_XXX_ACTIVITY_TIMELINE_MENU` | [Пункт контекстного меню](*CRM_XXX_ACTIVITY_TIMELINE_MENU) дела в карточке элемента ||
|| `CRM_XXX_ROBOT_DESIGNER_TOOLBAR` | [Пункт выпадающего меню](*CRM_XXX_ROBOT_DESIGNER_TOOLBAR) верхней кнопки дизайнера роботов ||
|| `CRM_FUNNELS_TOOLBAR` | Пункт выпадающего [меню в туннелях продаж](*CRM_FUNNELS_TOOLBAR) ||
|| `CRM_ANALYTICS_MENU` | Пункт левого [меню CRM-аналитики](*CRM_ANALYTICS_MENU) ||
|| `CRM_ANALYTICS_TOOLBAR` | Пункт выпадающего меню [верхней кнопки CRM-аналитики](*CRM_ANALYTICS_TOOLBAR) ||
|| [Задачи](./task/index.md)  | > ||
|| `TASK_LIST_CONTEXT_MENU` | Пункт [контекстного меню](*TASK_LIST_CONTEXT_MENU) списка ||
|| `TASK_VIEW_TAB` | [Вкладка в карточке](*TASK_VIEW_TAB) задачи ||
|| `TASK_VIEW_SIDEBAR` | [Правая панель](*TASK_VIEW_SIDEBAR) карточки задачи ||
|| `TASK_VIEW_TOP_PANEL` | [Ссылка в верхней части](*TASK_VIEW_TOP_PANEL) карточки задачи ||
|| `TASK_USER_LIST_TOOLBAR` | Пункт основного [выпадающего меню в задачах пользователя](*TASK_USER_LIST_TOOLBAR) ||
|| `TASK_GROUP_LIST_TOOLBAR` | Пункт основного [выпадающего меню в задачах группы](*TASK_GROUP_LIST_TOOLBAR) ||
|| `TASK_ROBOT_DESIGNER_TOOLBAR` | Пункт основного выпадающего [меню около настроек роботов](*TASK_ROBOT_DESIGNER_TOOLBAR) ||
|| [Рабочие группы/проекты](./workgroups/index.md) | > ||
|| `SONET_GROUP_DETAIL_TAB` | Пункт основного выпадающего [меню проекта](*SONET_GROUP_DETAIL_TAB) ||
|| [Профиль пользователя](./user-profile/profile-menu.md) | > ||
|| `USER_PROFILE_MENU` | [Пункт контекстного меню](*USER_PROFILE_MENU) в профиле ||
|| `USER_PROFILE_TOOLBAR` | [Пункт контекстного меню](*USER_PROFILE_TOOLBAR) верхней кнопки профиля ||
|| [Календарь](./calendar.md)  | > ||
|| `CALENDAR_GRIDVIEW` | Пункт в списке [видов отображения календаря](*CALENDAR_GRIDVIEW) ||
|| [Телефония](./telephony/index.md) | > ||
|| `CALL_CARD` | [Вкладка](*CALL_CARD) в карточке звонка ||
|| `TELEPHONY_ANALYTICS_MENU` | [Пункт меню](*TELEPHONY_ANALYTICS_MENU) в аналитике звонков ||
|| [Контакт-центр](./contact-center.md) | > ||
|| `CONTACT_CENTER` | [Виджет в контакт-центре](*CONTACT_CENTER)||
|#




[*CRM_XXX_LIST_MENU]:![Виджет в виде пункта контекстного меню в Сделке](crm/_images/CRM_DEAL_LIST_MENU.png "Виджет в виде пункта контекстного меню в Сделке")
[*CRM_XXX_LIST_TOOLBAR]:![Виджет в виде пункта контекстного меню в Сделке](crm/CRM__LIST_TOOLBAR.png "Виджет в виде пункта контекстного меню в Сделке")
[*CRM_XXX_DETAIL_TAB]:![Виджет в виде вкладки в детальной карточке элемента CRM](crm/_images/CRM_DEAL_DETAIL_TAB.png "Виджет в виде вкладки в детальной карточке элемента CRM")
[*CRM_XXX_DETAIL_ACTIVITY]:![Виджет в виде пункта меню таймлайна в Сделке](crm/_images/CRM_DEAL_DETAIL_ACTIVITY.png "Виджет в виде пункта меню таймлайна в Сделке")
[*CRM_XXX_DETAIL_TOOLBAR]:![Виджет в виде пункта выпадающего меню верхней кнопки карточки сделки](crm/_images/CRM_DEAL_DETAIL_TOOLBAR.png "Виджет в виде пункта выпадающего меню верхней кнопки карточки сделки")
[*CRM_XXX_ACTIVITY_TIMELINE_MENU]:![Виджет в виде пункта контекстного меню дела в лиде](crm/_images/CRM__ACTIVITY_TIMELINE_MENU.png "Виджет в виде пункта контекстного меню дела в лиде")
[*CRM_XXX_ROBOT_DESIGNER_TOOLBAR]:![Виджет в виде пункта выпадающего меню верхней кнопки дизайнера роботов](crm/_images/CRM_ROBOT_DESIGNER_TOOLBAR.png "Виджет в виде пункта выпадающего меню верхней кнопки дизайнера роботов")
[*CRM_FUNNELS_TOOLBAR]:![Виджет в виде пункта в тулбаре туннелей продаж](crm/_images/CRM_FUNNELS_TOOLBAR.png "Виджет в виде пункта в тулбаре туннелей продаж")
[*CRM_ANALYTICS_MENU]:![Виджет в виде пункта списка приложений CRM-аналитики](crm/_images/CRM_ANALYTICS_MENU.png "Виджет в виде пункта списка приложений CRM-аналитики")
[*CRM_ANALYTICS_TOOLBAR]:![Виджет в виде пункта в тулбаре CRM-аналитики](crm/_images/CRM_ANALYTICS_TOOLBAR.png "Виджет в виде пункта в тулбаре CRM-аналитики")
[*TASK_LIST_CONTEXT_MENU]:![Виджет в виде пункта контекстного меню списка](task/_images/TASK_LIST_CONTEXT_MENU.png "Виджет в виде пункта контекстного меню списка")
[*TASK_VIEW_TAB]:![Виджет в виде вкладки в карточке задачи](task/_images/TASK_VIEW_TAB.png "Виджет в виде вкладки в карточке задачи")
[*TASK_VIEW_SIDEBAR]:![Виджет в виде пункта правой панели карточки задачи](task/_images/TASK_VIEW_SIDEBAR.png "Виджет в виде пункта правой панели карточки задачи")
[*TASK_VIEW_TOP_PANEL]:![Виджет в виде пункта в верхней части карточки задачи](task/_images/TASK_VIEW_TOP_PANEL.png "Виджет в виде пункта в верхней части карточки задачи")
[*TASK_USER_LIST_TOOLBAR]:![Виджет в виде пункта в основном выпадающем меню в задачах пользователя](task/_images/TASK_USER_LIST_TOOLBAR.png "Виджет в виде пункта в основном выпадающем меню в задачах пользователя")
[*TASK_GROUP_LIST_TOOLBAR]:![Виджет в виде пункта в основном выпадающем меню в задачах группы](task/_images/TASK_USER_LIST_TOOLBAR.png "Виджет в виде пункта в основном выпадающем меню в задачах группы")
[*TASK_ROBOT_DESIGNER_TOOLBAR]:![Виджет в виде пункта основного выпадающего меню около настроек роботов](task/_images/TASK_ROBOT_DESIGNER_TOOLBAR.png "пункта основного выпадающего меню около настроек роботов")
[*SONET_GROUP_DETAIL_TAB]:![Виджет в виде пункта основного выпадающего меню проекта](workgroups/_images/SONET_GROUP_DETAIL_TAB.png "Виджет в виде пункта основного выпадающего меню проекта")
[*CALENDAR_GRIDVIEW]:![Виджет в виде пункта в списке видов отображения календаря](_images/CALENDAR_GRIDVIEW.png "Виджет в виде пункта в списке видов отображения календаря")
[*CALL_CARD]:![Виджет в виде пункта во вкладке карточки звонка](telephony/_images/CALL_CARD.png "Виджет в виде пункта во вкладке карточки звонка")
[*TELEPHONY_ANALYTICS_MENU]:![Виджет в виде пункта меню в аналитике звонков](telephony/_images/TELEPHONY_ANALYTICS_MENU.png "Виджет в виде пункта меню в аналитике звонков")
[*USER_PROFILE_MENU]:![Виджет в виде пункта в контекстном меню в профиле](user-profile/_images/USER_PROFILE_MENU.png "Виджет в виде пункта в контекстном меню в профиле")
[*USER_PROFILE_TOOLBAR]:![Виджет в виде пункта в контекстном меню верхней кнопки профиля](user-profile/_images/USER_PROFILE_TOOLBAR.png "Виджет в виде пункта в контекстном меню верхней кнопки профиля")
[*CONTACT_CENTER]:![Виджет в виде пункта в списке Контакт-центра](_images/CONTACT_CENTER.png "Виджет в виде пункта в списке Контакт-центра")