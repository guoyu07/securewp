---
layout: post
title: Заголовок X-Content-Type-Options: nosniff
date: 2014-12-26
category: .htaccess
tags: [.htaccess, application/ecmascript, application/javascript, application/x-javascript, content-type, drive-by-downloads, Header, MIME, MIME-sniffing, MIME-type, MIME-type confusion, nosniff, text/css, text/ecmascript, text/javascript, text/jscript, text/vbs, text/vbscript, text/x-javascript, X-Content-Type-Options]
canonical: https://securemywp.ru/2014/12/26/заголовок-x-content-type-options-nosniff/
---

Еще один рекомендованный заголовок ответа сервера: `X-Content-Type-Options: nosniff` препятствует броузеру загружать стили и скрипты с неправильно заданным MIME типом (поддерживают IE и Chrome).
Соответственно:
```apache
<IfModule mod_headers.c>
Header set X-Content-Type-Options nosniff
</IfModule>
```
[Подробности…](http://msdn.microsoft.com/en-us/library/ie/gg622941(v=vs.85).aspx)

Если коротко, при наличии этого заголовка броузер не станет загружать стиль, если его MIME-type не `"text/css"` и не будет загружать скрипт, если его MIME-type не один из:
```
"application/ecmascript"
"application/javascript"
"application/x-javascript"
"text/ecmascript"
"text/javascript"
"text/jscript"
"text/x-javascript"
"text/vbs"
"text/vbscript"
```
[Подробнее](https://htaccess.wordpress.com/2009/09/22/x-content-type-options-nosniff-header/)
