---
layout: post
title: Переименовываем wp-login.php
date: 2014-12-08
category: wp-login.php
tags: [.htaccess, general-template.php, RedirectMatch, wp-login.php, обфускация]
canonical: https://securemywp.ru/2014/12/08/переименовываем-wp-login-php/
---

Войти в панель управления можно по-разному, но общая точка входа — файл [/wp-login.php](http://codex.wordpress.org/Function_Reference/wp_login_form).

Разумеется, все боты и все любители начинают именно с этого адреса. Есть смысл этот файл переименовать во что-нибудь длинно-хитрое, полученное от генератора паролей, вроде `I05gfJnBCIYDaGJjbW0y.php`. В самом этом файле редактором делаем
`search & replace 'wp-login.php' -> 'I05gfJnBCIYDaGJjbW0y.php'` (без кавычек).

Точно такую же замену вхождений `wp-login.pgp` на `I05gfJnBCIYDaGJjbW0y.php` надо сделать в файле `/wp-includes/general-template.php`.

Входить в панель управления теперь будем через `/I05gfJnBCIYDaGJjbW0y.php`. Поскольку броузер адреса запоминает, это обычно неудобств не несет. И есть смысл сохранить имя точки входа в менеджере паролей вместе с паролем.

Хотя файла `wp-login.php` в корне сайте теперь нет, запрет доступа к нему в `.htaccess` лучше оставить, чтобы в ответ на попытки входа отдавалась 403 ошибка, а не 404 страница, это существенно сэкономит паразитный трафик:

```html
RedirectMatch 403 /login\.php$
```

При всей непритязательности, это весьма эффективный фильтр доступа.

Плагины:
[Rename wp-login.php (unmaintained)](https://wordpress.org/plugins/rename-wp-login/)
