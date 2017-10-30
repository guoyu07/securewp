---
layout: post
title: bloginfo(‘version’)
date: 2014-12-08
category: themes
tags: [bloginfo, Header, header.php, version]
canonical: https://securemywp.ru/2014/12/08/bloginfoversion/
---

Если в файле <code>header.php</code> активной темы присутствует что-то такое:

<pre><code>
<meta name="generator" content="WordPress <?php bloginfo('version'); ?>" />
</code></pre>

 - лучше убрать.
