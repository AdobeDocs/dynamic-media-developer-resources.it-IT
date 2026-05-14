---
description: Controllo cache. Consente di disabilitare in modo selettivo la memorizzazione nella cache lato client (browser, server proxy, sistemi di memorizzazione nella cache di rete) e la memorizzazione nella cache interna [!DNL Platform Server] .
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
TQID: 'https://experienceleague.adobe.com/X6q0OKRjjjpgNxl8XDuzkNBzrzTBS4E5BtXQGuJWgmk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
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
