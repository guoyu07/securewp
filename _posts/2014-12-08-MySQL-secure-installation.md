---
layout: post
title: MySQL secure installation
date: 2014-12-08
category: mysql
tags: [MySQL, mysql_secure_installation]
canonical: https://securemywp.ru/2014/12/08/mysql-secure-installation/
---

Еще до установки вордпресса, сразу после установки <code>MySQL</code> надо его [слегка обезопасить](http://rifco.ru/blog/2013/12/23/mysql-после-установки/).

Для этого надо запустить <code>mysql_secure_installation</code> — удалить анонимных пользователей, запретить удаленное подключсение. Если этого не сделать,останется лишняя лазейка.
