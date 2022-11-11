---
description: Controllo della cache. Consente di disattivare selettivamente la memorizzazione in cache lato client (browser, server proxy, sistemi di memorizzazione in cache di rete) e la memorizzazione in cache interna [!DNL Platform Server] cache.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# cache{#cache}

Controllo della cache. Consente di disattivare selettivamente la memorizzazione in cache lato client (browser, server proxy, sistemi di memorizzazione in cache di rete) e la memorizzazione in cache interna [!DNL Platform Server] cache.

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

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

Se solo uno *`cacheControl`* viene specificato, viene applicato sia alle cache client che a quelle server.

Attributo di richiesta. Ignorato quando la richiesta non restituisce un&#39;immagine di risposta. *`clientControl`* viene ignorato quando la memorizzazione in cache lato client è disabilitata dal catalogo immagini (se `catalog::Expiration` ha un valore negativo).

Il valore predefinito è `cache=on,on`.
