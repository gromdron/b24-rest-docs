# Подключение и использование BX24.js

Если ваше приложение реализует пользовательский интерфейс внутри Битрикс24 (выводится на специальной странице или использует инструменты встройки), то вы можете воспользоваться возможностями специальной JS-библиотеки. Она:
- во-первых, представляет собой JS SDK для REST, что позволяет обращаться к REST прямо из front-end вашего приложения не погружаясь в [реализацию авторизации](https://dev.1c-bitrix.ru/learning/course/index.php?COURSE_ID=99&CHAPTER_ID=05379&LESSON_PATH=8771.5379) по OAuth 2.0,
- во-вторых, предлагает ряд дополнительных функций для взаимодействия пользовательского интерфейса вашего приложения с интерфейсом Битрикс24:
  - управление размером фрейма,
  - вызов стандартных диалогов,
  - и т.п.

Подключается библиотека следующим образом:

```js
<script src="//api.bitrix24.com/api/v1/"></script>
```

Для внешних приложений и вебхуков библиотека использоваться не может.