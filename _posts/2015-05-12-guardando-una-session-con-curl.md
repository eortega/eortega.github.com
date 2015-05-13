---
layout: post
title: "Guardando una sesión con curl"
description: "Como guardar una sesión de usuario con Curl en CLI"
category: How-To
tags: [Curl, Command Line, CLI ]
---
{% include JB/setup %}

Utilizando las opciones -D y -b con curl 

Para guardar una sesión utilizar -D data_session_file

{% highlight ruby  %}
~ curl -D file_to_save_session -d "usuario=yo&password=secreto" http:api.test/login
{% endhighlight %}


Para Utilizar la información guardada utilizar -b data_session_file
{% highlight ruby %}
~ curl -b file_to_save_session  http:api.test/account
{% endhighlight %}
