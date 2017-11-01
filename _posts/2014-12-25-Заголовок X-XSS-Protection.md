---
layout: post
title: Заголовок X-XSS-Protection
date: 2014-12-25
category: htaccess
tags: [.htaccess, Cross Site Scripting, Header, X-XSS-Protection, XSS, XSS Protection, Межсайтовый скриптинг]
canonical: https://securemywp.ru/2014/12/25/заголовок-x-xss-protection/
---

Для защиты от некоторых типов XSS-атак (Межсайтовый скриптинг) рекомендуется добавить такой заголовок в ответы сервера: `X-XSS-Protection: 1; mode=block`, добавив в `.htaccess`:

```html
<IfModule mod_headers.c>
Header set X-XSS-Protection "1; mode=block"
</IfModule>
```
