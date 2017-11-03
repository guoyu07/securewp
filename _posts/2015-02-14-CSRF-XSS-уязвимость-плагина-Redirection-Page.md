---
layout: post
title: CSRF/XSS уязвимость плагина Redirection Page
date: 2015-02-14
category: plugins
tags: [Cross Site Request Forgery, Cross Site Scripting, CSRF, POST, Redirection Page, XSS]
canonical: https://securemywp.ru/2015/02/14/csrf-xss-уязвимость-плагина-redirection-page/
---

Уязвимость типа `CSRF/XSS` в плагине [Redirection Page](https://wordpress.org/plugins/redirection-page/) до версии 1.2. Плагин позволяет сделать редирект конкретной страницы.

Уязвимость основана на хранении несанированных данных. Уязвимость позволяет злоумышленнику изменить настройки перенаправления, направив зарегистрированного пользователя на специально созданную страницу с помощью специального POST-запроса вида:

```
/wp-admin/options-general.php?page=redirection-page&redirectionpage_action=add
```

[Подробности](http://packetstormsecurity.com/files/130314/WordPress-Redirection-Page-1.2-CSRF-XSS.html)…
