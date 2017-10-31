---
layout: post
title: XML-RPC Pingback для DDoS-атак
date: 2015-12-17
category: functions.php
tags: [add_filter, functions.php, pingback, pingback.ping, XML-RPC, xmlrpc_methods, xmlrpc.php]
canonical: https://securemywp.ru/2015/12/17/xml-rpc-pingback-для-ddos-атак/
---

Мы уже [упоминали](http://securemywp.ru/2014/12/18/отключаем-xml-rpc/) опасности, связанные с <code>XML-RPC</code>, и что для большей безопасности этот сервис лучше совсем отключить. Однако, его отключение лишает и некоторых удобств, связанных с ним, в частности, использование альтернативных клиентов (вроде <code>WLW, [Windows Live Writer](https://ru.wikipedia.org/wiki/Редактор_блогов_Windows_Live)</code>), а также мобильных приложений для администрирования сайта. Поэтому, в большинстве случаев <code>XML-RPC</code> остается работать.

В упомянутом выше посте речь шла о возможной уязвимости самого модуля <code>XML-RPC</code> и его использовании для проникновения на ваш сайт. Но этот модуль можно использовать и иначе, для того, чтобы ваш сайт стал средством атаки на другие сайты и [был включен](http://habrahabr.ru/post/215543/) в <code>DDoS</code>-ботсеть, причем даже без взлома.

Воспрепятствовать этому можно, отключив метод <code>pingback</code> модуля <code>XML-RPC</code>. Для этого надо в <code>functions.php</code> активной темы вставить фрагмент:
<pre><code>
add_filter( 'xmlrpc_methods', function( $methods ) {
unset( $methods['pingback.ping'] );
return $methods;
} );
</code></pre>
