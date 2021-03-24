---
description: Immagine mappa Gloss. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordo o decal ripetibili.
solution: Experience Manager
title: mappa lucida
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---


# glossmap{#glossmap}

Immagine mappa Gloss. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordo o decal ripetibili.

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;parentesi graffa;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;race;'&amp;race;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> ForeignReq</span>'&amp;rbrace;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Gloss map image file (scala di grigi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Richiedi a Image Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>Richiedi a un server esterno. </p></td> 
 </tr> 
</table>

Applicabile a materiali quali effetti di vernice metallica, sfondi e bordi di lamina tagliata, tessuti metallici e così via.

L&#39;immagine della mappa lucida deve essere in scala di grigi a 8 bit e avere esattamente le stesse dimensioni dell&#39;immagine principale specificata con `src=`. Per ulteriori informazioni, fare riferimento alla descrizione di [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) .

## Proprietà {#section-26375672d69849be9b026cc93c3bc558}

Attributo materiale. Supportato da texture ripetibili, sfondi e bordi e decalcomanie. Ignorati da materiali di rivestimento in tinta unita, armadio e finestre. Per ulteriori informazioni, consulta [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) .

## Predefinito {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Nessuno.

## Consultate anche {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
