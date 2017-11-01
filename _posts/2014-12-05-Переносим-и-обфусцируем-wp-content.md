---
layout: post
title: Переносим и обфусцируем wp-content
date: 2014-12-05
category: wp-config.php
tags: [dirname(__FILE__), document_root, wp-config.php, wp-content]
canonical: https://securemywp.ru/2014/12/05/переносим-и-обфусцируем-wp-content/
---

В папке `wp-content` размещаются темы, плагины, загруженные пользователями файлы. Ее можно перенести и переименовать, например так:
```php
define( 'WP_CONTENT_DIR', dirname(__FILE__) . '/uJYvBWPZCuBTvjMIlrno' );
```

Это должно быть веб-доступное место, урл которого тоже следует определить:

```php
define( 'WP_CONTENT_URL', 'http://example/uJYvBWPZCuBTvjMIlrno' );
```

В этом примере сам конфиг размещается — `dirname(__FILE__)` — [на уровень выше](https://securemywp.ru/2014/12/04/убираем-конфиг-наверх/) `document_root`.

Это мероприятие требует некоторой осторожности. Некоторые разработчики плагинов (возможно, и тем) могут не предполагать такой возможности и пользоваться стандартным расположением и наименованием `wp-config`.

Ну и не забываем перенести все содержимое на новое место вручную.
