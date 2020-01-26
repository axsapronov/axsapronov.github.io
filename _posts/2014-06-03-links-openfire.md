---
layout: post
title: "Ссылки. Openfire"
description: "Набор ссылок по разработке плагинов для Openfire"
category: ссылки 
tags: [ссылки, development, openfire, jabber]
---


<!--more-->

### Введение

**Openfire** — это XMPP-сервер, написанный на Java. 

Официальная страница - [http://www.igniterealtime.org/projects/openfire/](http://www.igniterealtime.org/projects/openfire/)

Сервер особо не видел в бою. До 1к одновременных коннектов на среднем железе держал. А большие нагрузки на своих глазах не видел.
Писал для него на коленках простые плагины. 


### Инструкции

* [Как собирать плагины для openfire](https://community.igniterealtime.org/docs/DOC-1200)
* [Установка openfire на ubuntu 12.04](http://www.thefanclub.co.za/how-to/how-setup-instant-messaging-server-using-openfire-ubuntu-1204)
* [Сбросить настройки](http://serverfault.com/questions/365258/how-to-reset-openfire-data) - я например забыл пароль админа сразу же.
* [Пример nginx config для openfire](https://raw.githubusercontent.com/arthurfurlan/nginx-config-templates/master/openfire.conf)


### Инструкции для разработки плагинов

Немного ботов для затравки:

* [Jabber-бот для Openfire за час](http://habrahabr.ru/post/52523/) - дает понимание структуры плагинов, а также некоторых взаимодействий
* [Botz: Internal Bot Library for Openfire](https://community.igniterealtime.org/docs/DOC-1130) - описание библиотеки бота
* [Helga (a Server-Bot plugin)](https://community.igniterealtime.org/docs/DOC-1080) - еще один бот

Более направленные инструкции:

* [Openfire Plugin Development: Message of the Day](http://www.igniterealtime.org/support/articles/motd_plugin.jsp) - несколько прояснет возможности сообщений
* [Гайд по разработке плагинов](http://www.igniterealtime.org/builds/openfire/docs/latest/documentation/plugin-dev-guide.html) - структура бывает путает. Ибо в реальных плагинах может быть другая

Плагин userservice хороший путь для разбора на примере программирование сервлетов

* [Описание возможностей плагина userservice](http://www.igniterealtime.org/projects/openfire/plugins/userservice/readme.html)

#### Частные случаи разработки

Одним из плагинов было обеспечение работы с Apple Push Notification
Мне помогли ссылки:  

* [Полная документация](http://www.igniterealtime.org/projects/openfire/documentation.jsp) - все что может пригодиться
* [Документация](https://developer.apple.com/library/ios/documentation/iphone/conceptual/iphoneosprogrammingguide/ManagingYourApplicationsFlow/ManagingYourApplicationsFlow.html) - объясняется что и как работает в этой системе
* [Руководство по работе с Apple Push Notification Service](http://habrahabr.ru/company/ruswizards/blog/156811/) - информация о том, где брать и куда вставлять какие-то ключи. А также проясняется что есть два вида ключей, это для разработки и для продакшена
* [Особенности работы с Apple push notification service](http://habrahabr.ru/post/157481/) - для общего развития помогает


Примеры кода

* [Пример реализации Push Natification](http://www.aayug.com/2013/08/push-notification-for-ios-and-android.html) - дает первый код



Уже полуготовые библиотеки:

* [java-apns](https://github.com/notnoop/java-apns) - на основе этой библиотеки написал плагин для Apple Push Notification
* [javapns](https://code.google.com/p/javapns/) - проще чем первая, но у меня не запустилось (с паролями что-то заглючила она)

### Возможные проблемы при разработке и их решения

* [https://community.igniterealtime.org/thread/47895](https://community.igniterealtime.org/thread/47895)


### Ссылки
* [Набор плагинов из стандартной поставки и чуть больше](http://www.igniterealtime.org/projects/openfire/plugins.jsp) - у большинства можно найти и исходники