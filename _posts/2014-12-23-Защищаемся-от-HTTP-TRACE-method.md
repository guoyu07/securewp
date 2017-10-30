---
layout: post
title: Защищаемся от HTTP TRACE method
date: 2014-12-23
category: htaccess
tags: [.htaccess, Cross Site Scripting, Cross Site Tracing, Header, HTTP, TRACE, XSS, XST]
canonical: https://securemywp.ru/2014/12/23/защищаемся-от-http-trace-method/
---

Есть техника атаки, называемая [Cross Site Tracing](http://www.cgisecurity.com/whitehat-mirror/WH-WhitePaper_XST_ebook.pdf) (<code>XST</code>), используемая вместе с так называемым <code>Cross Site Scripting (XSS)</code> на основе запросов <code>HTTP TRACE</code>. Эта возможность может быть включена на многих серверах для отладки, что позволяет через HEADER-запросы получить важную информацию от вашего сервера.
Лучше вовсе исключить TRACE-запросы:

<pre><code>
RewriteEngine On
RewriteCond %{REQUEST_METHOD} ^TRACE
RewriteRule .* - [F]
</code></pre>

[Подробнее](http://www.apacheweek.com/issues/03-01-24#news)…
