---
description: Immagine mappa lucida. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordi o decali ripetibili.
seo-description: Immagine mappa lucida. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordi o decali ripetibili.
seo-title: glossario
solution: Experience Manager
title: glossario
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# glossmap{#glossmap}

Immagine mappa lucida. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordi o decali ripetibili.

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;parentesi graffa;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;race;'&amp;rrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> </span>externalReq'&amp;race;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>File immagine mappa lucida (scala di grigio). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Richiedete a Image Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> externalReq  </span> </span> </p></td> 
  <td class="stentry"> <p>Richiesta a un server esterno. </p></td> 
 </tr> 
</table>

Applicabile a materiali quali effetti di vernice metallica, sfondi e bordi di pellicola tagliati a stampo, tessuti di fili metallici e così via.

L&#39;immagine della mappa lucida deve essere in scala di grigio a 8 bit e avere esattamente le stesse dimensioni dell&#39;immagine principale specificata con `src=`. Per ulteriori informazioni, fare riferimento alla descrizione di [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca).

## Proprietà {#section-26375672d69849be9b026cc93c3bc558}

Attributo materiale. Supportato da texture ripetibili, sfondi e bordi e decali. Ignorata dai materiali di rivestimento in tinta unita, armadio e finestre. Per ulteriori informazioni, vedere [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca).

## Predefinito {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Nessuno.

## Consultate anche {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
