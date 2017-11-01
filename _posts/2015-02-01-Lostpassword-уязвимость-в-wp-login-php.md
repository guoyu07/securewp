---
layout: post
title: Lostpassword уязвимость в wp-login.php
date: 2015-02-01
category: core
tags: [CSRF, lostpassword, Password Reset, rp_key, wp-login.php]
canonical: https://securemywp.ru/2015/02/01/lostpassword-уязвимость-в-wp-login-php/
---

Уязвимость в форме восстановления пароля в файле `/wp-login?action=lostpassword`, выявлена в ноябре 2014 г. Тип уязвимости `CSRF`. Устранена введением нового параметра `rp_key`.

Уязвимость действительна вплоть до версии вордпресса 4.0, устранена в версии 4.0.1.

Подробности [здесь](https://core.trac.wordpress.org/changeset/30418).
