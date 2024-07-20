---
description: Controllo cache. Consente di disabilitare in modo selettivo la memorizzazione nella cache lato client (browser, server proxy, sistemi di memorizzazione nella cache di rete) e la memorizzazione nella cache interna [!DNL Platform Server] .
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# cache{#cache}

Controllo cache. Consente di disabilitare in modo selettivo la memorizzazione nella cache lato client (browser, server proxy, sistemi di memorizzazione nella cache di rete) e la memorizzazione nella cache interna di [!DNL Platform Server].

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> attivato|disattivato</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> attivato|disattivato</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> controllo server</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> attivato|disattivato</span> </p></td> 
 </tr> 
</table>

Se viene specificato un solo valore *`cacheControl`*, verrà applicato sia alle cache client che a quelle server.

Attributo della richiesta. Ignorato quando la richiesta non restituisce un’immagine di risposta. *`clientControl`* viene ignorato quando il caching lato client è disabilitato dal catalogo immagini (se `catalog::Expiration` ha un valore negativo).

Impostazione predefinita: `cache=on,on`.
