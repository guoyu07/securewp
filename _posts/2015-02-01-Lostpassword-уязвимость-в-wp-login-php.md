---
layout: post
title: Lostpassword уязвимость в wp-login.php
date: 2015-02-01
category: core
tags: [CSRF, lostpassword, Password Reset, rp_key, wp-login.php]
canonical: https://securemywp.ru/2015/02/01/lostpassword-уязвимость-в-wp-login-php/
---

Уязвимость в форме восстановления пароля в файле <code>/wp-login?action=lostpassword</code>, выявлена в ноябре 2014 г. Тип уязвимости <code>CSRF</code>. Устранена введением нового параметра <code>rp_key</code>.

Уязвимость действительна вплоть до версии вордпресса 4.0, устранена в версии 4.0.1.

Подробности [здесь](https://core.trac.wordpress.org/changeset/30418).
