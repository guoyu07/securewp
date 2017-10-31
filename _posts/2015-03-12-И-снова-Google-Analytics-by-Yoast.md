---
layout: post
title: И снова Google Analytics by Yoast
date: 2015-03-12
category: plugins
tags: [Cross Site Scripting, Google Analytics, javascript, manual_ua_code_field, XSS, Yoast]
canonical: https://securemywp.ru/2015/03/12/и-снова-google-analytics-by-yoast/
---

Мы уже сообщали о <code>XSS</code> уязвимости плагина [Google Analytics](https://wordpress.org/plugins/google-analytics-for-wordpress/) от [Team Yoast](https://yoast.com/), исправленной в версии 5.1.3. Тогда уязвимость была связана с отсутствием санации вводимого сохраняемого поля <code>manual_ua_code_field</code>.

В текущей версии 5.3.2 также присутствует сходная уязвимость в хранимом поле для самостоятельного ввода кода <code>Google Analytics</code> «<code>Manually enter your UA code</code>», обнаружена в феврале 2014, пока не исправлена.

Особенно можно не беспокоиться, поскольку значение уязвимого поля вводится вручную администратором, то есть уязвимость может быть доступна злоумышленнику лишь при весьма специфических обстоятельствах.

[Подробнее](http://packetstormsecurity.com/files/130716/).
