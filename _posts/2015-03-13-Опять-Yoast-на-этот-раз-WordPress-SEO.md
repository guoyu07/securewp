---
layout: post
title: Опять Yoast, на этот раз WordPress SEO
date: 2015-03-13
category: plugins
tags: [Blind SQL Injection, class-bulk-editor-list-table.php, esc_sql, orderby, sanitize_text_field, WordPress SEO, Yoast]
canonical: https://securemywp.ru/2015/03/13/опять-yoast-на-этот-раз-wordpress-seo/
---

Другой популярный плагин от [Team Yoast](https://yoast.com/), [WordPress SEO](https://wordpress.org/plugins/wordpress-seo/) оказался уязвимым. Уязвимость обнаружена в марте 2014 г., действительна вплоть до версии 1.7.3.3, в текущей версии 1.7.4 устранена.

Уязвимость типа `Blind SQL Injection` присутствует в файле `admin/class-bulk-editor-list-table.php`. Параметры `orderby` и `order`, получаемые из GET-параметров, перед использованием в SQL-запросе не санируются должным образом. Уязвимость основана на недостаточности санации на основе встроенных функций `sanitize_text_field()` и `esc_sql()`.

Подробности [здесь](https://wpvulndb.com/vulnerabilities/7841).
