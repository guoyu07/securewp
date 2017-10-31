---
layout: post
title: Опять Yoast, на этот раз WordPress SEO
date: 2015-03-13
category: plugins
tags: [Blind SQL Injection, class-bulk-editor-list-table.php, esc_sql, orderby, sanitize_text_field, WordPress SEO, Yoast]
canonical: https://securemywp.ru/2015/03/13/опять-yoast-на-этот-раз-wordpress-seo/
---

Другой популярный плагин от [Team Yoast](https://yoast.com/), [WordPress SEO](https://wordpress.org/plugins/wordpress-seo/) оказался уязвимым. Уязвимость обнаружена в марте 2014 г., действительна вплоть до версии 1.7.3.3, в текущей версии 1.7.4 устранена.

Уязвимость типа <code>Blind SQL Injection</code> присутствует в файле <code>admin/class-bulk-editor-list-table.php</code>. Параметры <code>orderby</code> и <code>order</code>, получаемые из <code>GET</code>-параметров, перед использованием в <code>SQL</code>-запросе не санируются должным образом. Уязвимость основана на недостаточности санации на основе встроенных функций <code>sanitize_text_field()</code> и <code>esc_sql()</code>.

Подробности [здесь](https://wpvulndb.com/vulnerabilities/7841).
