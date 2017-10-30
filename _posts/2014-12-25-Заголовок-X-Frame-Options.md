---
layout: post
title: Заголовок X-Frame-Options
date: 2014-12-25
category: htaccess
tags: [.htaccess, ClickJacking, Header, IfModule, SAMEORIGIN, X-Frame-Options]
canonical: https://securemywp.ru/2014/12/25/заголовок-x-frame-options/
---

Для защиты от так называемого [ClickJacking](https://ru.wikipedia.org/wiki/Кликджекинг), когда контент вашего сайта встраивается (<code>iframe</code>) на странице другого сайта, рекомендуется добавить такой заголовок в ответе сервера: <code>X-Frame-Options: SAMEORIGIN</code>, например так (в <code>.htaccess</code>):

<pre><code>
<IfModule mod_headers.c>
Header always append X-Frame-Options SAMEORIGIN
</IfModule>
</code></pre>

В этом случае во фрейме будет показываться только содержимое с этого же сайта.

Если вы не используете <code>iframe</code> на своем сайте, можно вместо <code>SAMEORIGIN</code> использовать значение <code>DENY</code>, тогда во фрейме вообще ничего нельзя вывести.

Но бывает удобно вставить в <code>iframe</code>, например, pdf-документ.

[Подробнее](https://blog.mozilla.org/security/2013/12/12/on-the-x-frame-options-security-header/)… [Еще подробнее](http://blogs.msdn.com/b/ieinternals/archive/2010/03/30/combating-clickjacking-with-x-frame-options.aspx)…
