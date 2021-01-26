---
description: Controllo cache. Consente di disattivare selettivamente la memorizzazione nella cache lato client (browser, server proxy, sistemi di cache di rete) e la memorizzazione nella cache interna del server della piattaforma.
seo-description: Controllo cache. Consente di disattivare selettivamente la memorizzazione nella cache lato client (browser, server proxy, sistemi di cache di rete) e la memorizzazione nella cache interna del server della piattaforma.
seo-title: cache
solution: Experience Manager
title: cache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# cache{#cache}

Controllo cache. Consente di disattivare selettivamente la memorizzazione nella cache lato client (browser, server proxy, sistemi di cache di rete) e la memorizzazione nella cache interna del server della piattaforma.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Se viene specificato un solo valore *`cacheControl`*, questo viene applicato sia alle cache client che a quelle del server.

Attributo di richiesta. Ignorato quando la richiesta non restituisce un&#39;immagine di risposta. *`clientControl`* viene ignorato quando la memorizzazione nella cache sul lato client è disabilitata dal catalogo immagini (se  `catalog::Expiration` ha un valore negativo).

Il valore predefinito è `cache=on,on`.
