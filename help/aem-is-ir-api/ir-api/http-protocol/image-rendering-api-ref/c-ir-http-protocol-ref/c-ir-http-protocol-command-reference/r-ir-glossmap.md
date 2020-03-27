---
description: Immagine mappa lucida. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordi o decali ripetibili.
seo-description: Immagine mappa lucida. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordi o decali ripetibili.
seo-title: glossario
solution: Experience Manager
title: glossario
topic: Scene7 Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# glossario{#glossmap}

Immagine mappa lucida. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordi o decali ripetibili.

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{'is{'<span class="varname"> isReq</span>'}|{'{'<span class="varname"> ForeignReq</span>'}' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span></span> </p></td> 
  <td class="stentry"> <p>File immagine mappa lucida (scala di grigio). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span></span> </p></td> 
  <td class="stentry"> <p>Richiedete a Image Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> externalReq </span></span> </p></td> 
  <td class="stentry"> <p>Richiesta a un server esterno. </p></td> 
 </tr> 
</table>

Applicabile a materiali quali effetti di vernice metallica, sfondi e bordi di pellicola tagliati, tessuti metallici e così via.

L’immagine della mappa lucida deve essere in scala di grigio a 8 bit e avere esattamente le stesse dimensioni dell’immagine principale specificata con `src=`. Per ulteriori informazioni, fare riferimento alla descrizione di [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) .

## Proprietà {#section-26375672d69849be9b026cc93c3bc558}

Attributo materiale. Supportato da texture ripetibili, sfondi e bordi e decali. Ignorata da colori solidi, armadio e rivestimenti per finestre. Consultate [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) per ulteriori informazioni.

## Predefinito {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Nessuno.

## Consultate anche {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
