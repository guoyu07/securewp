---
layout: post
title: Переносим и обфусцируем wp-content
date: 2014-12-05
category: wp-config.php
tags: [dirname(__FILE__), document_root, wp-config.php, wp-content]
canonical: https://securemywp.ru/2014/12/05/переносим-и-обфусцируем-wp-content/
---

В папке <code>wp-content</code> размещаются темы, плагины, загруженные пользователями файлы. Ее можно перенести и переименовать, например так:
<pre><code>
define( 'WP_CONTENT_DIR', dirname(__FILE__) . '/uJYvBWPZCuBTvjMIlrno' );
</code></pre>

Это должно быть веб-доступное место, урл которого тоже следует определить:

<pre><code>
define( 'WP_CONTENT_URL', 'http://example/uJYvBWPZCuBTvjMIlrno' );
</code></pre>

В этом примере сам конфиг размещается — <code>dirname(__FILE__)</code> — [на уровень выше](https://securemywp.ru/2014/12/04/убираем-конфиг-наверх/) <code>document_root</code>.

Это мероприятие требует некоторой осторожности. Некоторые разработчики плагинов (возможно, и тем) могут не предполагать такой возможности и пользоваться стандартным расположением и наименованием <code>wp-config</code>.

Ну и не забываем перенести все содержимое на новое место вручную.
