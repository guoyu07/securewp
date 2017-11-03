---
layout: post
title: Заголовок X-Frame-Options
date: 2014-12-25
category: htaccess
tags: [.htaccess, ClickJacking, Header, IfModule, SAMEORIGIN, X-Frame-Options]
canonical: https://securemywp.ru/2014/12/25/заголовок-x-frame-options/
---

Для защиты от так называемого [ClickJacking](https://ru.wikipedia.org/wiki/Кликджекинг), когда контент вашего сайта встраивается (`iframe`) на странице другого сайта, рекомендуется добавить такой заголовок в ответе сервера: `X-Frame-Options: SAMEORIGIN`, например так (в `.htaccess`):

```apache
<IfModule mod_headers.c>
Header always append X-Frame-Options SAMEORIGIN
</IfModule>
```

В этом случае во фрейме будет показываться только содержимое с этого же сайта.

Если вы не используете `iframe` на своем сайте, можно вместо `SAMEORIGIN` использовать значение `DENY`, тогда во фрейме вообще ничего нельзя вывести.

Но бывает удобно вставить в `iframe`, например, pdf-документ.

[Подробнее](https://blog.mozilla.org/security/2013/12/12/on-the-x-frame-options-security-header/)… [Еще подробнее](http://blogs.msdn.com/b/ieinternals/archive/2010/03/30/combating-clickjacking-with-x-frame-options.aspx)…
