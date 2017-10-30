---
layout: post
title: Усиливаем wp-content
date: 2014-12-03
category: plugins
tags: [.htaccess, Allow, Deny, php, wp-content]
canonical: https://securemywp.ru/2014/12/03/усиливаем-wp-content/
---

Вообще говоря, извне должны запускаться лишь php-файлы движка. Файлы темы и плагинов должны запускаться самим движком. Но, строго говоря, это не обязательно так, точнее, зависит от разработчиков тем и плагинов.

В общем, есть смысл попробовать защитить от внешних вызовов <code>wp-content</code>, поместив в нем в <code>.htaccess</code>:

<pre><code>
<FilesMatch .php>
Order Deny,Allow
Deny from All
</Files>
</code></pre>

После этого надо внимательно посмотреть — правильно ли работают тема и плагины. Если да, оставляем. Если нет, переносим это же в папку <code>Uploads</code>, там уж точно сломать нечего, а какой-то смысл есть.
