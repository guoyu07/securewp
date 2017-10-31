---
layout: post
title: Server Side Request Forgery (SSRF) уязвимость Вордпресса
date: 2015-02-01
category: core
tags: [http.php, Server Side Request Forgery, SSRF, URL Validation, wp-includes]
canonical: https://securemywp.ru/2015/02/01/server-side-request-forgery-ssrf-уязвимость-вордпресса/
---

Уязвимость найдена в файле <code>/wp-includes/http.php</code> в функции проверки (валидации) <code>url</code>.

Уязвимость обнаружена в ноябре 2014 г. Действительна вплоть до версии 4.0 (исправлено в версии 4.0.1). [Подробности](https://core.trac.wordpress.org/changeset/30444)…
