---
layout: post
title: "Debugueando Curl en PHP"
description: "Encontrando la mejor manera para debuguear las peticiones realizadas con CURL desde PHP"
category: How To
tags: [curl, php, ]
---
{% include JB/setup %}

http://www.tuxradar.com/practicalphp/15/10/4

{% highlight php linenos %}
<?php
       $curl = curl_init();
        $url ="https://api.mercadolibre.com/sites/MLA/categories";
        curl_setopt ($curl, CURLOPT_URL, $url);
        curl_setopt($curl, CURLOPT_RETURNTRANSFER, 1);
        curl_setopt($curl, CURLOPT_VERBOSE, 1);
        //curl_setopt($curl, CURLOPT_SSLVERSION, 3);
        $data=json_decode(curl_exec ($curl));


        if(!curl_errno($curl)){
                $info = curl_getinfo($curl);
                print_r($info);
        }else{
                print_r(curl_getinfo($curl));
        }

        curl_close ($curl);
    
?>
{% endhighlight %}

Segundo caso
http://stackoverflow.com/questions/3757071/php-debugging-curl

Buena herramienta para probar que protocolos y versiones acepta un dominio (API)
https://www.ssllabs.com/ssltest/
