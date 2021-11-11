[![Build status](https://ci.appveyor.com/api/projects/status/ikam6m5bhv3xsy1j?svg=true)](https://ci.appveyor.com/project/PerochenkoVA/ci-json-api)


Про JAR

Важно: если вы работаете на Windows с Турецкой локалью и при запуске учебных приложений получаете Exception вида:

Caused by: java.lang.NoSuchFieldException: wrıteHandlerReference (тут не английская i, а именно ı или ?)
at java.lang.Class.getDeclaredField(Unknown Source)
at java.util.concurrent.atomic.AtomicReferenceFieldUpdater$AtomicReferenceFieldUpdaterImpl$1.run(Unknown Source)
at java.util.concurrent.atomic.AtomicReferenceFieldUpdater$AtomicReferenceFieldUpdaterImpl$1.run(Unknown Source)
at java.security.AccessController.doPrivileged(Native Method)
... 21 more
Тогда вам все JAR'ники нужно будет запускать командой:

java -Duser.language=en -Duser.country=US -jar app-mbank.jar
Часть -jar app-mbank.jar может меняться, но первая часть для вас во всех ДЗ (при запуске на вашем ПК будет именно такой).


**Задача №1 - Настройка CI**
AppVeyor

**Задача №2 - JSON Schema**
JSON Schema предлагает нам инструмент валидации JSON-документов. С описанием вы можете познакомиться по этому адресу: https://json-schema.org/understanding-json-schema/index.html