---
layout: post
title: MySQL secure installation
date: 2014-12-08
category: mysql
tags: [MySQL, mysql_secure_installation]
canonical: https://securemywp.ru/2014/12/08/mysql-secure-installation/
---

Еще до установки вордпресса, сразу после установки `MySQL` надо его [слегка обезопасить](http://rifco.ru/blog/2013/12/23/mysql-после-установки/).

Для этого надо запустить `mysql_secure_installation` — удалить анонимных пользователей, запретить удаленное подключсение. Если этого не сделать,останется лишняя лазейка.
